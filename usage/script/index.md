---
layout: page
title: Using OpenSheetMusicDisplay
permalink: /usage/script/
lang: en_US
---

> This page focuses on using OpenSheetMusicDisplay as global library via script tag. For usage with module bundlers, take a look at the [TypeScript guide](/usage/typescript) instead.

Download the latest OpenSheetMusicDisplay bundle from [Github](https://github.com/opensheetmusicdisplay/opensheetmusicdisplay/releases/latest) and include it in your page via script tag. The following snippet shows how to load and display a MusicXML from a remote location.
```html
<script src="osmd.min.js"></script>
<script>
  var osmd = new opensheetmusicdisplay.OSMD("container-id");
  osmd
    .load("http://downloads2.makemusic.com/musicxml/MozaVeilSample.xml")
    .then(
      function() {
        osmd.render();
      }
    );
</script>
```

Depending on your Browser, you might encounter CORS issues when trying to load a MusicXML from a remote location. If that is the case, try to serve one from the script's location.
