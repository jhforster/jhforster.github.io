---
title: When simple & low tech is good enough
tags:
- product
---
My effort to commit fully to using Jekyll for all of my blogging needs has mostly worked and gone smoothly. It is in a good sweet spot for my technical abilities. I mostly understand it. My basic working knowledge of the command line, ruby, html, css, and git offer enough competence to get it working without too much fussing (usually).

But, more importantly, parts of it are a bit outside my current technical abilities. Sure, I encounter challenges. Often, in fact. But I perceive them as solvable challenges and so I'm motivated to do so. Flow state, deliberate practice, and all that stuff.

But not all challenges are worth solving.

As someone who has worked in Product for over a decade, I know this. It is obviously true at an intellectual level – there isn't time to solve all of the problems before us. Duh. And I feel confident coaching others through these types of trade-offs. Or being the decision maker on where we're drawing the line on an effort.

But it is harder when *you are* the one wrestling with the challenge directly. It is easier to maintain good judgment as a third-party. It is hard to do it yourself and self edit while working on something.

That is all to say – I spent **a lot of time** trying to figure out how to responsively embed media on this blog. It took me longer than it should have to realize the rabbit hole I was going down. It felt like a solvable challenge[^1] so I stubbornly insisted on trying to solve it.

But no solutions were presenting themselves. Some required moving off hosting on Github pages so I could use plugins, which means introducing a CI tool. Others required making a ton of custom CSS in various `_include` files or some crazy shit with javascript to handle the different aspect ratios of various sources. Lastly, some involved making API calls to oEmbed, which is a non-starter since this is a static site and not a server.

No solutions that met my needs or abilities[^2].

But in earlier in my googling, I had stumbled across iFramely. A paid service for solving this problem. I didn't want to pay for anything. But they offer a ["Check URL"][cu] page where you can paste in any link and it spits out responsive embed code...

I thought about it a bit more. On average, I only post a few times a week. And maybe only a third of those posts need to handle an embed. I'm not going to be doing this terribly often. How slick of a solution do I need?

So there you have it. Now when I find a link I'd like to share, I take 5 seconds to copy it into iFramely and paste the output. It is an extra step, sure. But it is simple and it works.

Sometimes, it is good to re-learn a lesson the hard way.

![](https://imgs.xkcd.com/comics/is_it_worth_the_time.png)

[^1]: And it still does, tbh – it is 2019 how hard can it be to embed links...
[^2]: This Jekyll codex has a "without plugins" section that looked very promising. It worked perfectly for Youtube links but Vimeo wasn't working for me. Beyond that, looking at the code for it, I did not feel confident that I could expand it to work with other services any time soon.

[cu]: https://iframely.com/embed
