---
layout: page
title: Roadmap
permalink: /develop/roadmap/
lang: en_US
---

## Done
* Draw layouted measures
* Draw Beams
* Draw Key, Clef, Rhythm Instructions
* Draw accidentals
* Draw System Lines
* at least the first connecting line.
* Draw Labels (Title, Composer, Instruments, ...) →  MusicSheetDrawer
* implement  TextMeasurer correctly
* implement renderLabel in VexFlowMusicSheetDrawer
* Create npm Package
* Draw play Cursor line    →  MusicSheetDrawer
* port new MusicSheetDrawer to TS
* implement renderRectangle in VexFlowMusicSheetDrawer
* implement simple iterator.moveNext() loop for demo.
* for redraw of cursor: call musicSheetDrawer.drawSheet(gms); again.
* Implement adapting to screen size. → call .calculate() of MusicSheetCalculator
* zooming
* Implement piece selector of 5 pre-selected pieces and file upload
* Inhouse: Refactor parameters of
  * createInstrumentBracket (upper, lower stave)
  * createGroupBracket (upper, lower stave)
* Draw Dots
* Draw Ties
* Draw Tuplets


## ToDo
* Fix wrong Tuplets x spacing (data not correctly given to Vexflow?)
* Fix drawing multiple ties of chords all above each other resulting in only one visible tie
* Draw Repetitions
  * Lines
  * Repetition Endings (horizontal brackets with Number-Label)
  * Words
* Draw Articulations (staccato, accent...)
* Draw Instrument Braces
* Draw Group Brackets
* Draw In-Staff Clefs
* Draw Grace notes (as small notes)
* Inhouse: Convert Tuplet label placement code to TS
* Inhouse: Convert Stem Direction calculator code to TS
* Inhouse: Refactor and Convert SkyBottomLineCalculator for systems y-size calculation to TS
* adapt y-layout code for using SkyBottomLineCalculator
* Draw Measure numbers
* Draw Chord Symbols
* Inhouse: Refactor and convert Slur Handling (handling special cases from tied and beamed notes)
* Draw Slurs
* Draw Word Expressions
  * Dynamics
  * Tempo
  * Other
* Draw Wedges
* Draw Lyrics
  * Words
  * Connecting dashes
  * extending underscores
* Draw Ornaments (trill, turn, ...)
* Tabs?
  * read from Xml
  * draw Tabs
