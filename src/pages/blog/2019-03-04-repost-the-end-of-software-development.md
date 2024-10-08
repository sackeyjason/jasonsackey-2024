---
title: "Repost: The end of software development"
date: "2019-03-04"
categories: 
  - "operating-system"
  - "programming"
layout: "./_layout.astro"
---

Computers, to be useful for any particular task, need software. The practice of creating that software, developing it, programming it, happens to be considered as a specialised one. That wasn’t always the case. Microcomputers (PCs from the 70s and 80s) used to boot into a programming environment, such as some variety of BASIC. [The user manual that came with the Commodore 64](http://www.lemon64.com/manual/) included programming instructions. The expectation was that, to a much greater extent than now, computer-users would be programmers. Programming, as in writing code, was part of standard procedure for operating a computer.

What’s changed?

The perception of the situation, at least. The division of labour here has intensified. Software development became a role separate and distinct from regular, productive uses of a computer. Everyone (including the developer) uses software created by others. That software may be generally available, for free or commercially. Or it might be developed bespoke.

An organisation that requires bespoke software for its business has several options. It can outsource the task to an external agency. It may decide to undertake the project in-house. It may have developers on staff ready to go. Or it may employ some, or train some.

These options aren’t really so distinct. A bespoke software project involving external developers will necessarily be a collaboration between the companies. It’ll involve training existing staff, because, clearly, they’ll need to learn to be able to use the new software. It didn’t exist before.

In theory, software development comes to an end when the project is done. The software’s functionality satisfies the requirements. Perhaps one day we’ll have all the software we need, and the role of ‘software developer’ will be obsolete.

Back to reality…

> Software is never finished. It is only abandoned.

Software projects tend to go through multiple phases of iterative development and use. Requirements evolve, so software needs to be adaptable. The substance of software is highly malleable, changeable stuff. Any possible program can, with the necessary code-changes, be transformed into any other. How easily that process can be done is a function of structural design and complexity. A well-designed, simpler system is more flexible.

One way to gain flexibility is to provide user-operable configuration.

Software is, to varying extents, configurable. That means a user may adjust its functionality within a set of defined (by the developer) parameters. This activity is generally considered part of ordinary usage of software. It doesn’t directly accomplish the purpose of the software. It serves the goal in a secondary way, if the adjustable options can be set to more preferred ones.

Configurability is a double-edged sword. The more configurable a system is, the more potential it has for users to adapt it to better serve their needs, without the need for specialised development skills. But a more powerful configurable system is more complex. Highly-complex system configuration becomes a specialised skill unto itself. Systems like Drupal allow different users to be restricted to subsets of the vast, intimidating array of available configuration features, for the sake of mental health, as well as for system security.

Maximal configurability is where the specialised developer works, i.e. a programming environment that permits unrestricted transformation of a system.

The task of incorporating new functionality, when exceeding the scope of configuration, of course falls to the programmer. The complexity of a system’s configuration options will be, to some extent, reflected in the structure of the program code. A more complex system is more difficult to adjust without breaking stuff. That means development work becomes more risky and expensive.

Reducing a system’s configurability, by removing unwanted options, makes a system simpler to use, potentially enhancing productivity and reducing training costs. The program-level aspect of this might involve deleting code, reducing the program’s overall size and complexity. For a developer, this is a very pleasing notion.

#### Feature creep and bloat

Consider this well-known dysfunction of software development, the tendency for a project to grow in scope excessively.

Growth is good when it means a software system gaining more capabilities in a healthy way. So I’ve qualified my description of ‘creep’ and ‘bloat’ to include the concept of _excess_. But what does that really mean?

We may use ‘feature creep’ or ‘scope creep’ to refer to a phenomenon in the course of the development process where new requirements are added, which isn’t a problem in and of itself. Problems arise when extra resources are inadequately allocated, and are thus stretched to excess. Some additional requirements and resource-stretching is to be expected in real-world software development. Keeping that within manageable limits falls to the discipline of project management. Totally eliminating ‘creep’ isn’t the point — adaptable, flexible software is what we’re trying to make, and that takes an adaptable, flexible development team.

Mature software systems that have grown well beyond their original version may be characterised as ‘bloated’. One might cite, in particular cases, objective, technical reasons for this designation. E.g.:

- it’s too resource-intensive; the software uses excessive processing, memory, bandwidth, etc.
- with rising complexity, it’s grown too difficult to use
- it’s code has grown too complex, stalling further development

These are all matters of judgment. Alas, the question of software bloat does not admit of clear, unambiguous answers derived from some universally-accepted calculation of factors.

Increasingly resource-intensive software can be run on better hardware.

Difficult-to-use software can be delivered with additional training.

A tangled, rusty codebase can be refactored, given sufficient development resources.

That is, if the project owner has the necessary resources to spend.

---

> [**Zawinski’s Law**](http://www.catb.org/jargon/html/Z/Zawinskis-Law.html)**:** “Every program attempts to expand until it can read mail. Those programs which cannot so expand are replaced by ones which can.” Coined by Jamie Zawinski (who called it the “Law of Software Envelopment”) to express his belief that all truly useful programs experience pressure to evolve into toolkits and application platforms (the mailer thing, he says, is just a side effect of that).

“We won’t have the resources to develop and maintain a mail-reader in our bee colony-monitoring application”. That line of argument might well be convincing to the director of the bee-management institution. Especially if we have supporting demonstrable calculations, as seems plausible in this case.

Dedicated teams are building mail software. Our bee system and some other mail system can be made to cooperate. Instead of duplicating their efforts, we want to make use of them, through APIs.

The efficiency argument seems clear.

So we have good reasons to resist the temptation to add non-core functionality to some system, where that functionality is arguably better-served by other software. Why does that temptation arise in the first place?

Modern operating systems provide filesystems. So, a user can draw a picture with a graphics program, save it to a file, then send that file to someone else using an email program. The developers of the graphics and email programs didn’t need to directly cooperate for that to happen.

This exemplifies the idea that with proper infrastructure provided by the lower-level system, a non-specialist software-user can take multiple programs and work with them in combination. When they can’t, then they need to call up specialist developers, systems integrators.

Sufficiently decentralised architecture will let non-specialist users combine a set of simple tools to achieve their desired system functionality. That’s the next frontier for the computing world, and seems to belong to the disciplines of designing operating systems and networks. As they evolve, certain sorts of specialised software development work will become obsolete. Then we’ll move to a new level of complex system-building.

#### Anticipated challenges

It’s not enough to merely invent or discover a better basic system architecture. You also need to convince other developers to cooperate, to write their software so it plays nicely in that new environment. How is that done? They need some inventive. The new system can’t be just a little bit better than existing alternatives with which developers are already quite comfortable, thankyouverymuch. It needs to be a vast leap in technical capability.

Or, you could pay them. Microsoft developers write programs for Microsoft’s Windows systems. They tried to encourage developer support for their phone platform by means of [cash incentives](https://www.windowscentral.com/microsoft-pay-out-100000-get-developers-coding-windows-phone). That initiative was [unsuccessful](https://www.theverge.com/2017/10/9/16446280/microsoft-finally-admits-windows-phone-is-dead). Maybe if they’d spent more money, it would have worked. Who can tell?

Most software development organisations lack the funds for this crude approach. But many companies besides Microsoft (and including them) invest much in the struggle for hearts and minds of software users, and that subset who are developers. Information technology is rife with rival schools of thought and the politicking which is necessary for their propagation.

[Ted Nelson has discussed this extensively and entertainingly](https://www.youtube.com/watch?v=KdnGPQaICjk):

> Every faction wants you to think they are the wave of the future and because there are no objective criteria, as in religion there are no objective criteria, there are thousands of sects and splinter groups.

When we’re trying to build something, shouldn’t our technological choices be determined by objective, factual, criteria? Certainly, we may agree on many facts about the present technological landscape. What about the future? We’re building the future. Its shape is indeterminate. It’s made of malleable stuff, and the process of its shaping is one of much creative freedom.

Or, if you’re a hardcore cynic, it _used to be_. The technologically-creative formations of yesterday shape and guide and [contrain](https://twitter.com/TheTedNelson/status/911414624523755521) our present-day options.

---

### Further reading:

[**Unix philosophy - Wikipedia**  
\_The Unix philosophy, originated by Ken Thompson, is a set of cultural norms and philosophical approaches to minimalist…\_en.wikipedia.org](https://en.wikipedia.org/wiki/Unix_philosophy)

#### … and watching:

https://www.youtube.com/watch?v=9cXTGW9J9a0

https://youtu.be/KdnGPQaICjk

<figure>

![](./images/90f06-1y46fyr-fsfztk4wo5xqzyw.jpeg)

<figcaption>

[Cole Thomas The Consummation The Course of the Empire 1836](https://en.wikipedia.org/wiki/The_Course_of_Empire_%28paintings%29)

</figcaption>

</figure>
