---
layout: demo
title: Demo
permalink: /demo/
menu: main
order: 4
customJS:
  - demo.min.js
---

<!-- ## MusicXML input
OSMD can display [MusicXML][0] in both `.xml` and `.mxl` containers. On this demo page, you can either choose from the list of music below or just drop your own MusicXML on this page.

## Renderer
You can select the rendering strategy, by choosing either the Canvas option, or the SVG one.

## Zoom level
You control the zoom level of the music sheet displayed. Right now, OSMD is rendering the music piece at <span id="zoom-str">100</span>% on <span id="size-str">0</span>px width.

## Cursor
OSMD is able to display a simple cursor. You can control the visibility of the cursor and navigate through the piece using the following controls. You can also use the right arrow key to step through the piece.
-->

<h3 class="centered" id="header"> <img alt="OSMD logo" align="center" height="40" src="https://github.com/opensheetmusicdisplay/opensheetmusicdisplay/assets/33069673/a83dc850-65c2-4c7a-8836-eb75cefc006f"/> OpenSheetMusicDisplay Demo </h3>
<div id="versionDiv" class="version-div centered">OSMD Version: </div>
<!-- version inserted in js -->
<div class="button group">
  <div class="control-container">
    <h4 class="centered">Cursor</h4>
    <input type="button" value="Show" id="show-cursor-btn" class="btn btn-demo"/>
    <input type="button" value="Hide" id="hide-cursor-btn" class="btn btn-demo"/>
    <input type="button" value="Back" id="previous-cursor-btn" class="btn btn-demo"/>
    <input type="button" value="Next" id="next-cursor-btn" class="btn btn-demo"/>
    <input type="button" value="Reset" id="reset-cursor-btn" class="btn btn-demo"/>
  </div>
  <div class="control-container">
    <h4 class="centered">Zoom</h4>
    <input type="button" value="Zoom In" id="zoom-in-btn" class="btn btn-demo"/>
    <input type="button" value="Zoom Out" id="zoom-out-btn" class="btn btn-demo"/>
    <p id="zoom-str">100</p>
  </div>
  <div class="control-container">
    <h4 class="centered">Renderer</h4>
    <select id="backend-select" class="btn btn-demo" value="svg">
        <option value="svg">SVG</option>
        <option value="canvas">Canvas</option>>
    </select>
    <input type="button" value="Re-Render" id="debug-re-render-btn" class="btn btn-demo"/>
    <input type="button" value="Clear" id="debug-clear-btn" class="btn btn-demo"/>
    <input type="button" value="Create PDF" id="print-pdf-btn" class="btn btn-demo"/>
  </div>
  <div class="control-container">
    <h4 class="centered">Select score</h4>
    <select id="selectSample" class="btn btn-demo"></select>
    <h4 class="centered">Or just drop your own MusicXML on this page.</h4>
  </div>
</div>
<div id="error-tr" class="error-container">
  <div id="error-td"></div>
</div>
<div class="demo-canvas" id="osmd-demo-canvas"></div>

[0]: https://www.musicxml.com/
