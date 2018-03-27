---
layout: page
title: Roadmap
permalink: /develop/roadmap/
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
* Fix wrong Tuplets x spacing (data not correctly given to Vexflow?)
* Draw Chord Symbols
* Draw Lyrics
  * Words
  * Connecting dashes
* Draw Repetitions
  * Barlines
  * Words (Segno, Fine)
* Draw Articulations (staccato, accent...)
* Draw Instrument Braces
* Draw Group Brackets
* Inhouse: Convert Stem Direction calculator code to TS
* Draw Tabs
  * read from Xml
  * draw Tabs

## ToDo
* Fix drawing multiple ties of chords all above each other resulting in only one visible tie
* Fix Tabs x-layout for rest notes for correct x alignment with normal notes
* Draw Repetition Endings (horizontal brackets with Number-Label)
* Draw In-Staff Clefs
* Draw Grace notes (as small notes)
* Implement Plugin Infrastructure
* Inhouse: Convert Tuplet label placement code to TS
* Inhouse: Refactor and Convert SkyBottomLineCalculator for systems y-size calculation to TS
* adapt y-layout code for using SkyBottomLineCalculator
* Draw Measure numbers
* Inhouse: Refactor and convert Slur Handling (handling special cases from tied and beamed notes)
* Draw Slurs
* Draw Word Expressions
  * Dynamics
  * Tempo
  * Other
* Draw Wedges
* Draw Lyrics
  * extending underscores
* Draw Ornaments (trill, turn, ...)

## ToDo - Plugins (licensable from us)
* Implement Playback Plugin
  * Set start position (via click onto a note on the score)
  * set end position (for looping)
  * set speed in BPM
  * play back a metronome together with the music (with pre-count)
  * Playback of given chord symbols
  * Solo, Mute switches and volume settings for all instruments, the metronome and the chords (if avaliable)
  * React on repetitions (backjumps), on dynamics (p, ff) and tempo instructions
* Implement Transposition Plugin
  * Transpose whole score by a given number of semitones
  * Key signatures will be transposed
* Implement Midi Import Plugin
  * Read in a midi file for score rendering
