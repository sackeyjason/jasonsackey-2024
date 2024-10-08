---
title: Migrating this site from WordPress to Astro
date: '2024-10-08'
layout: "./_layout.astro"
---

It's about time.

I've had this site on WordPress for a while. I used wordpress.com - a cheap paid plan, so I could get rid of the ads. It was fine - I even made use of the block editor to customise the homepage. Most of the content was the blog, so it was a suitable platform.

Now I want something simpler, but that something that gives me (as a frontend developer) more control.

The recent WPEngine vs Automattic dispute is another factor.

## Technical stuff

First task: get the content. WP lets us export content to a big XML file. So I got my content in this format. Then what?

[wordpress-export-to-markdown](https://github.com/lonekorean/wordpress-export-to-markdown)

First result on Google. Easy peasy. Now I have my markdown files, with frontmatter for titles and dates, and tags and categories.

I prepended my blog files with the date in YYYY-MM-DD format (the best format). So sorting them by name means sorting chronologically.

Some gotchas:

- The date values came as strings. If you make a new post and use an unquoted date - the formatting will be different. You'll need to manually convert dates into Date objects, then format them, for consistency.
- You'll want to add a layout field. I did it manually.

Now I need blog listing code. Here it is:

```astro
---
const allPosts = await Astro.glob("./*.md");
allPosts.reverse();
const postList = allPosts.map((post) => {
    return {
        url: post.url,
        title: post.frontmatter.title,
        date: post.frontmatter.date,
    };
});
---

<h1>Blog</h1>

<ul>
    {
        postList.map((post) => (
            <li>
                <a href={post.url}>
                    {post.title} - {post.date}
                </a>
            </li>
        ))
    }
</ul>
```

Work in progress, more details TBC.
