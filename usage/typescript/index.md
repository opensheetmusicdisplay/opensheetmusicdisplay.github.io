---
layout: page
title: Using OSMD with TypeScript
permalink: /usage/typescript/
---

[TypeScript][0] in combination with [Webpack][1], [SystemJS][2] or [Browserify][3], is the most comfortable and straightforward way of using OpenSheetMusicDisplay.

> An up-to-date example of how to use OpenSheetMusicDisplay with TypeScript and Webpack can be found in the [webpack-usage-example](https://github.com/opensheetmusicdisplay/webpack-usage-example) repository. Examples for SystemJS and RequireJS are available under [systemjs-usage-example](https://github.com/opensheetmusicdisplay/systemjs-usage-example) and [browserify-usage-example](https://github.com/opensheetmusicdisplay/browserify-usage-example).

Retrieve the lastest version of OpenSheetMusicDisplay from npm:
```sh
$ npm install --save opensheetmusicdisplay
```

In your TypeScript source, import the `OpenSheetMusicDisplay` class from the `opensheetmusicdisplay` module
```typescript
import { OpenSheetMusicDisplay } from "opensheetmusicdisplay";
```
and instantiate it with the DOM element to contain the music sheet:
```typescript
let openSheetMusicDisplay = new OpenSheetMusicDisplay(container);
```
Note that [`OpenSheetMusicDisplay`'s constructor][constructor] either takes an element's ID as string or the actual `HTMLElement` as first parameter.

Now we can load MusicXML by either passing a file's URL, the root node of a MusicXML
document or the string content of a `.xml` or `.mxl` file to [`OpenSheetMusicDisplay`'s `load()` method][load].
```typescript
openSheetMusicDisplay
  .load("http://downloads2.makemusic.com/musicxml/MozaVeilSample.xml")
  .then(
    () => openSheetMusicDisplay.render(),
    (err) => console.err(err)
  )
  .then(
    () => console.log("Sheet music displayed."),
    (err) => console.err(err)
  );
```
[`load()`][load] returns a Promise, and as soon as loading the sheet music finishes successfully,
[`OpenSheetMusicDisplay`][OpenSheetMusicDisplay] can be instructed to render it by calling [`render()`][render]. Note that [`render()`][render] returns a Promise too, which can be used to take further actions on finish or handle errors.

[0]:           https://www.typescriptlang.org/
[1]:           https://webpack.js.org/
[2]:           https://github.com/systemjs/systemjs
[3]:           http://browserify.org/
[load]:        /classdoc/classes/osmd.html#load
[OSMD]:        /classdoc/classes/osmd.html
[constructor]: /classdoc/classes/osmd.html#constructor
[render]:      /classdoc/classes/osmd.html#render
