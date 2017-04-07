---
layout: post
title:  "OpenSheetMusicDisplay Preview: this is going to happen over the next months"
date:   2016-03-12 00:00:00
author: Thomas Buchstätter
---

[MusicXML][2] is the most popular file format to store, archive, publish and share sheet music on the internet. It is open source and supported worldwide by hundreds of applications.

Here is a process visualization of how to make [MusicXML][2] files appear as digital sheet music on your screen:

![OSMD Engine Process Visualization](/assets/osmd_process.svg)

We have already developed native Android and iOS apps (PhonicScore lite, please see our [website][0] for more info) in the past for reading and displaying [MusicXML][2] with C# and Xamarin.

For our new web app [PracticeBird][3] we want to build on existing music rendering web technologies. This is where [VexFlow][1] comes into play. We love [VexFlow][1], it has just one downside: there is no working [MusicXML][2] parser. Thus we decided to build one and open it to the public.

Moreover we extend the parser’s functionalities and name the whole project _Open Sheet Music Display_ – the first open source sheet music rendering engine that can display your [MusicXML][2] files on your web page!

The version will read and display sheet music to any screen size. It will be ready in May.

Later releases will include responsive line breaks, zooming, display of titles and overlays eg. a moving cursor bar when playing audio.

We value open source software and its community. We will release OpenSheetMusicDisplay under MIT license.

See the timeline for more information on major development steps.

## Links

* Follow us on GitHub: [https://github.com/opensheetmusicdisplay](https://github.com/opensheetmusicdisplay)
* PhonicScore Apps: [http://www.phonicscore.com][0]

[0]: http://www.phonicscore.com/
[1]: http://www.vexflow.com/
[2]: https://www.musicxml.com/
[3]: https://www.practicebird.com/
