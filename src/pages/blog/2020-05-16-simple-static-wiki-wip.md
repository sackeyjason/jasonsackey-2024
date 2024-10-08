---
title: "Simple static wiki [WIP]"
date: "2020-05-16"
categories: 
  - "javascript"
tags: 
  - "hypertext"
  - "wiki"
layout: "./_layout.astro"
---

I'm setting up a lightweight wiki for dumping notes on miscellaneous topics up to a website as a set of arbitrarily-linked pages.

Here's my first pass solution, using the [Eleventy/11ty static site generator](https://www.11ty.dev/docs/).

https://github.com/sackeyjason/mcwiki

11ty converts the markdown into HTML files (in folders too). It also does templating, which I've yet to get my head around.

The main wiki-ish thing I'm looking for is quick linking. So I've added a shortcode for this.

Here's my (only) bit of config for that:

```
module.exports = function(eleventyConfig) {
  // Liquid Shortcode
  eleventyConfig.addShortcode("link", function(title) {
    const slug = title.toLowerCase()
      .split(" ")
      .join("-");
    return `<a href="/${slug}">${title}</a>`;
  });
};
```

So, `{% link 'personal wiki' %}` gets turned into an HTML link: `<a href="/personal-wiki">personal wiki</a>`

The syntax isn't ideal. It's kind of clunky. I'd rather have \[\[this style of link\]\], the double-square-brackets markup, used in [FedWiki](https://github.com/fedwiki/wiki), [Zim](https://zim-wiki.org/manual/Help/Wiki_Syntax.html), and [Roam](https://roamresearch.com/), invented by [UseMod](http://usemod.com/cgi-bin/wiki.pl), I think.

But that syntax isn't part of any of the template languages that 11ty supports. Perhaps this can be achieved via a plugin.

Another feature I'm looking to include in this thing:

https://mobile.twitter.com/swyx/status/1186485327516577793

Fixing all broken links with stub pages, automatically.

---

I'm not commited to sticking with the 11ty way of doing this. Here are my requirements:

- content source is a flat directory of text (markdown) files
- output is a website usable without JavaScript in the browser... so probably not React
- easy linking between pages

I'm not wedded to static HTML generation (but the portability of this approach makes it valuable). I'm not allergic to databases nor dynamic serverside stuff.

Hosting will be on Github Pages for now.
