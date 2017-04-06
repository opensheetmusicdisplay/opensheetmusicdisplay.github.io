---
layout: page
title: Demo
permalink: /demo/
menu: main
order: 4
customJS:
  - osmd-debug.js
  - demo.js
---

## MusicXML input
OSMD can display [MusicXML][0] in both `.xml` and `.mxl` containers. On this demo page, you can either choose from the list of music below or just drop your own MusicXML on this page.

<select id="select" class="btn btn-demo"></select>

## Zoom level
You control the zoom level of the music sheet displayed. Right now, OSMD is rendering the music piece at <span id="zoom-str">100</span>% on <span id="size-str">0</span>px width.

<input type="button" value="Zoom In" id="zoom-in-btn" class="btn btn-demo"/>
<input type="button" value="Zoom Out" id="zoom-out-btn" class="btn btn-demo"/>

## Cursor
OSMD is able to display a simple cursor. You can control the visibility of the cursor and navigate through the piece using the following controls. You can also use the right arrow key to step through the piece.

<input type="button" value="Show" id="show-cursor-btn" class="btn btn-demo"/>
<input type="button" value="Hide" id="hide-cursor-btn" class="btn btn-demo"/>
<input type="button" value="Next" id="next-cursor-btn" class="btn btn-demo"/>
<input type="button" value="Reset" id="reset-cursor-btn" class="btn btn-demo"/>

## Sheet music
<div id="error-container" class="error-container">This is really shit.</div>
<div id="osmd-demo-canvas"></div>

[0]: https://www.musicxml.com/
