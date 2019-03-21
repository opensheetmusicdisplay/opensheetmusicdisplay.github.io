---
layout: page
title: Roadmap
permalink: /develop/roadmap/
---

## Done (OSMD 0.7.8):
(list may be incomplete, see [Changelog](https://github.com/opensheetmusicdisplay/opensheetmusicdisplay/blob/develop/CHANGELOG.md))
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
* Draw Measure numbers
<!-- OSMD 0.5.0 -->
* Draw Repetition Endings (horizontal brackets with Number-Label)
* Draw In-Staff Clefs
* Draw Grace notes (as small notes)
* Draw Slurs
* Draw Word Expressions (mostly done)
  * Dynamics
  * Tempo
  * Other
* Draw Lyrics
  * extending underscores
* Draw Ornaments (trill, turn, ...)
* Draw Arpeggios
* Draw Wedges

## ToDo
(list may be incomplete, see [OSMD Issues](https://github.com/opensheetmusicdisplay/opensheetmusicdisplay/issues) and try filtering for the Feature Label)
* 1.0 feature set: See [OSMD 1.0 Github project](https://github.com/opensheetmusicdisplay/opensheetmusicdisplay/projects/3)

* Fix drawing multiple ties of chords all above each other resulting in only one visible tie
* Fix Tabs x-layout for rest notes for correct x alignment with normal notes

* Ability to combine two notes into one notehead (e.g. one notehead with two stems, one up, one down)
* Implement Plugin Infrastructure
* Inhouse: Convert Tuplet label placement code to TS
* Inhouse: Refactor and Convert SkyBottomLineCalculator for systems y-size calculation to TS
* adapt y-layout code for using SkyBottomLineCalculator
* Inhouse: Refactor and convert Slur Handling (handling special cases from tied and beamed notes)

## ToDo - Plugins (licensable?)
* Implement Playback Plugin
  * Set start position (via click onto a note on the score)
  * Set end position (for looping)
  * Set speed in BPM
  * Play back a metronome together with the music (with pre-count)
  * Playback of given chord symbols
  * Solo, Mute switches and volume settings for all instruments, the metronome and the chords (if avaliable)
  * React on repetitions (backjumps), on dynamics (p, ff) and tempo instructions
* Implement Transposition Plugin
  * Transpose whole score by a given number of semitones
  * Key signatures will be transposed
* Implement Midi Import Plugin
  * Read in a midi file for score rendering
