---
layout: post
title:  "5 Reasons why we decided to build the first open source JavaScript engine for MusicXML using VexFlow"
date:   2016-04-14 00:00:00
author: Thomas Buchstätter
lang:   en_US
---

Every developer building solutions for digital sheet music using JavaScript sooner or later stumbles across [VexFlow][1]:

> VexFlow is an open-source online music notation rendering API. It is written completely in JavaScript, and runs right in the with browser. VexFlow supports HTML5 Canvas and SVG.
>
> -- <cite>vexflow.com</cite>

Here at PhonicScore we were like “Great, just what we needed! Oh wait, no MusicXML support? Impossible, there must be something?”

Trust me, there is nothing useful out there, yet.

As a music tech startup adding a web app to our [fleet of MusicXML sheet readers][0], we know how hard it is to build and maintain everything from scratch. At [PhonicScore][0] we love to work with VexFlow in order to avoid inventing the wheel twice. Unfortunately VexFlow does not support [MusicXML][2]. We are strong believers in MusicXML. Users / consumers / musicians also opted for this format.

Thus we decided to build our own open source JavaScript engine for MusicXML using VexFlow.

Here are five reasons that led to this decision:

## 1. VexTab does not read MusicXML
VexTab is a language also created by the creator of VexFlow to quickly create, edit, and render standard notation and guitar tablature that comes with VexFlow. VexTab is responsible for reading text commands and calculating the sheet music which is then rendered by VexFlow.

VexTab is proprietary and not free for commercial usage. Meh.

## 2. No MusicXML JavaScript parser available
There are two promising solutions: Dan Ringwalt’s [VexFlow MusicXML Plugin][3] and Taehoon Moon’s [Concerto Project][4]. We took a close look at both. It turned out that both would need a complete overhaul.

## 3. Reward for non open source software
On February 8, 2016 VexFlow issued a $5,000 bounty for creating a MusicXML Parser for VexFlow.

The downside?

> If you win, you must transfer full ownership of the code to me. This means that you may be unable to use, build derivative works from, or redistribute any code developed for this bounty.”
>
> -- <cite>https://github.com/0xfe/vexflow/issues/323</cite>

We feel that in the future displaying sheet music on the web should be wholesale jerseys common knowledge like it is displaying this piece of text in your browser.

## 4. Web app “Practice Bird”
Our new product [Practice Bird][5] is a practice log for musicians. As a web app we need to display sheet music in web browsers.


## 5. We love community
A great community already evolved around VexFlow. A recent comment on GitHub shows that there is strong need for a MusicXML parser:

> Why don’t we all, everyone in this thread who expressed interest in building this but having it stay open-source, build it together openly on github? […]
>
> -- <cite>Mike Turley on GitHub, March 24, 2016 https://github.com/0xfe/vexflow/issues/323#issuecomment-200930175</cite>

What are we waiting for? Let’s get started and build this together!

[0]: http://www.phonicscore.com/
[1]: http://www.vexflow.com/
[2]: https://www.musicxml.com/
[3]: https://github.com/ringw/vexflow
[4]: https://github.com/panarch/concerto
[5]: https://www.practicebird.com/
