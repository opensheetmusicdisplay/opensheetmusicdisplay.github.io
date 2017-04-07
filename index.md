---
title: OpenSheetMusicDisplay
layout: default
subtitle: The first JavaScript engine for MusicXML using VexFlow.
---

## About OpenSheetMusicDisplay

OpenSheeMusicDisplay is the missing link between MusicXML and VexFlow. Built upon many years of experience in both sheet music interactivity and engraving, it is the perfect solution for app developers seeking to build digital sheet music services.

MusicXML is the de facto standard for sharing sheet music on the internet. VexFlow is widely used for rendering sheet music. It features an extensive note sign library attributable to its open source nature.

OpenSheetMusicDisplay brings the two together and offers an open source turnkey solution for your digital sheet music project.


## Quick start

### Script tag
```html
<script src="osmd.min.js"></script>
<script>
var osmd = new OSMD("container-id");
osmd.load("http://downloads2.makemusic.com/musicxml/MozaVeilSample.xml").then(
  function() {
    osmd.render();
  }
);
</script>
```

### NPM & TypeScript
```sh
# Install the global CLI and its peer dependency
npm install --save opensheetmusicdisplay
```

```typescript
// In your TypeScript source file
import { OSMD } from "opensheetmusicdisplay";

let osmd = new OSMD(container, false);
osmd.load(...);
osmd.render();
```

Check out [the full usage guide](usage/script) to learn more.

[0]: http://www.typescriptlang.org/
