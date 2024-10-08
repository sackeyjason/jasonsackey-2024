---
title: "On hypertext, its origins, as it is, and as it could be"
date: "2019-02-18"
categories: 
  - "interface"
  - "network"
  - "the-stack"
  - "user"
  - "web"
tags: 
  - "hypertext"
  - "publishing"
layout: "./_layout.astro"
---

> EVERYTHING IS DEEPLY [INTERTWINGLED](https://en.wikipedia.org/wiki/Intertwingularity). In an important sense there are no "subjects" at all; there is only all knowledge, since the cross-connections among the myriad topics of this world simply cannot be divided up neatly.
>
> **— Ted Nelson, Computer Lib/Dream Machines 1974**

#### What is hypertext?

The term was coined by Ted Nelson, ‘to mean a body of written or pictorial material interconnected in such a complex way that it could not conveniently be presented or represented on paper.’ \[1\]

According to the founder of the World Wide Web, Tim Berners-Lee, hypertext is: ‘Nonsequential writing; Ted Nelson’s term for a medium that includes links. Nowadays it includes other media apart from text and is sometimes called hypermedia.’ \[2\]

Ideas about non-linear ways of representing information, stemming from the desire to transcend constricting structures that tend to be imposed by writing, precede those guys. They precede the invention of the computer. But it was computer technology that enabled a blossoming of [competing hypertext projects](https://en.wikipedia.org/wiki/Hypertext#Implementations), various network protocols and commercial software products.

Here I’ll talk about two of these, the web and Xanadu.

[Xanadu](http://xanadu.com/) is Nelson’s own baby, founded in 1960. The Xanadu vision is one of a publicly-accessible, globally-distributed archive of knowledge that preceded the Internet. It included an identity and payment system. Content in Xanadu could be accessed for free, or rightsholders could require payment for (permanent) access.

Xanadu documents would be linked together, and links were to be two-directional. Another sort of document linking was ‘transclusion’, a method for quoting a text that always links back to the original source. As these features imply, Xanadu content would be, by necessity, permanent. Documents could be added to, but never deleted (wholly or partially).

While the Xanadu project suffered setbacks over the years, Berners-Lee’s Web beat it to market. Born in the ’90s and flourishing well into the 2010s, it has prevailed as the champion in the global hypertext system competition.

Nelson still persistently pursues his own alternative. He’s developed incisive criticisms of the web, and of other parts of our prevailing computer paradigm.

[https://qz.com/778747/an-early-internet-pioneer-says-the-construction-of-the-web-is-crippling-our-thinking/](https://qz.com/778747/an-early-internet-pioneer-says-the-construction-of-the-web-is-crippling-our-thinking/)

I recommend his YouTube series, [Computers for Cynics](https://www.youtube.com/watch?v=KdnGPQaICjk&t).

#### Hypertext in the web

HTML, Hypertext Markup Language, is the basic substance of Web pages. Traditionally, HTML documents include all the readable text for a page, plus ‘markup’, which provides extra information to the browser concerning structural semantics — e.g. the start and end points for paragraphs, heading text, lists, and _stress emphasis_.

The primary hypertext-ish thing about HTML is one piece of markup, the <a> tag. It’s used to make links. Web links are wholly contained within their pages. They can link to sections within the page, or out to other pages. Nothing constrains the author of a page from linking to pages anywhere else on the Web, whether they’re on the same site, or on another one on a different server, on a different continent, and controlled by an unrelated party.

Web links are one-way, so for me to link to your site from mine, there’s no need for your site to coordinate with mine. It functions unilaterally. You might remove your page, and then my link becomes broken, ‘dead’ — the rest of my page remains fine, of course. I won’t know that the link is non-functional until someone tries to click it.

My act of linking to you doesn’t affect your site. At least not directly. Not until Google came along, but that’s another story (and here I’m not referring to the absurdity of news publishing companies wanting to [charge Google a levy for linking to their free content](https://savethelink.org/eu), but that’s worth mentioning; compare this with Xanadu, where the act publishing carries explicit permission to freely link content, and an integrated payment system is part of the basic infrastructure, potentially invaluable to the presently-suffering news industry.)

I highly recommend [_Lo and Behold_](https://www.youtube.com/watch?v=Bqx6li5dbEY) (video clip), the 2016 documentary about the Internet. Director and noted luddite Werner Herzog spoke with Ted Nelson for the film. We could sum up Ted’s critique of the Web and modern computing with the bold statement he gives:

> “_Humanity has no decent writing tools”_

Is this hyperbole? The best books in existence were probably written before computers existed. We’ve still got the low-tech writing tools. Computers have expanded our toolset. Ted’s written several influential books. I think this here essay is pretty good. Can we not claim that the writing tools we possess are serviceable, with room for improvement?

#### Hypertext: who needs it?

Well, look at this. Computers, being general-purpose machines, have done more than increase our writing capacity. They are everywhere, transforming all aspects of life in unpredictable ways. The game has changed. The landscape is shifting. There’s no possibility of being able to deal with this exponentially scaling complexity unless we level-up our writing (and/or thinking) methods.

Computers have already revolutionised writing, in some ways. Instantaneous global publication is an advance, for sure. And that’s yet another major contribution to the seemingly intractable miasma of context surrounding and bleeding into any particular subject matter you may care to address! That’s why I want something like Xanadu, a tool that manages text with natural, free-form interrelationality: allowing anything to be connected to anything else, without imposing linear or hierarchical structures. _Real_ hypertext.

Digital text system evolution has neglected the ‘deep structure’ that Nelson has been discussing since the ’60s, and instead nurtured development of presentational and decorative aspects: typefaces, page layout, animations, etc. He often seems to speak dismissively of such advances.

These things are why I have my job (as a frontend developer). And I love working on beautifully-designed stuff. Lacking a particular aptitude for visual design myself, I’m thankful that I get to work with great designers. I’m not as cynical as Ted about this stuff. What’s fuelling my view and agreement with Nelson is the opposite of cynicism, it’s a deep optimism that improvements to hypertext as we know it are possible, and will prove to be immensely valuable.

But here’s what a cynical view might look like.

1\. In the struggle to represent information about an increasingly complex world, we build a better text system. But couldn’t that just complete a cycle on an endless feedback loop of complexity-management tools generating more tangled complexity, necessitating the development of yet more sophisticated tooling, ultimately solving nothing?

2\. Consider the possibility that digital augmentation of the process of writing tends to degrade rather than improve it — distracting us, cluttering our perspectives, enabling useless information-hoarding.

(For a developer like me, there’s a temptation to use the lack of a decent hypertext system, a great CMS or a well-designed blog of my own, as an excuse to procrastinate rather than just write down what needs to be written. And on the other side, to use the lack of a cache of good writing to defer the development of that website to publish it…)

The original hypertext system is the human brain. Specifically a gifted, educated one. Interactive navigation of hypertext the old-fashioned way is: thinking or conversation. Can these natural capacities be significantly improved by mechanical automation?

We’ll keep trying, and find out.

---

Hundreds of companies are still working on expanding the capabilities of the web.

Lots of it is presentational stuff, like CSS layout functionality that’ll allow for more Magazine-like designs. There’s lots of features that enhance the Web as a software platform. People are working on virtual reality features.

And some stuff that’s more in the Xanadu direction: [annotation](https://hypothes.is/blog/annotation-is-now-a-web-standard/), [payments](https://www.w3.org/Payments/), [identity authentication](https://www.w3.org/community/w3id/). Finally!

Ted’s still working on Xanadu. The [latest implementation](http://xanadu.com/xuDemoPage.html) happens to be a web app.

---

1\. Theodor H, Nelson, “A File Structure for the Complex, the Changing and the Indeterminate,” Association for Computing Machinery: Proceedings of the 20th National Conference, 84–100. Ed. Lewis Winner, 1965.

2\. Tim Berners-Lee, Weaving the Web Glossary, 1999 [https://www.w3.org/People/Berners-Lee/Weaving/glossary.html](https://www.w3.org/People/Berners-Lee/Weaving/glossary.html)

N.B. I re-titled this essay today (13 November 2017) and demoted the original (hyperbolic, probably misunderstanding-provoking) title — Hypertext: who needs it — down to a subtitle.
