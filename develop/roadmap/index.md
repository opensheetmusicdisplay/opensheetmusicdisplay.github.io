OSMD Implementation Roadmap

Draw layouted measures
Draw Beams
Draw Key, Clef, Rhythm Instructions
Draw accidentals
Draw System Lines
at least the first connecting line.
Draw Labels (Title, Composer, Instruments, ...) →  MusicSheetDrawer
implement  TextMeasurer correctly
implement renderLabel in VexFlowMusicSheetDrawer
Create npm Package
Draw play Cursor line    →  MusicSheetDrawer
port new MusicSheetDrawer to TS
implement renderRectangle in VexFlowMusicSheetDrawer
implement simple iterator.moveNext() loop for demo.
for redraw of cursor: call musicSheetDrawer.drawSheet(gms); again.
Implement adapting to screen size. → call .calculate() of MusicSheetCalculator
zooming?
Implement piece selector of 5 pre-selected pieces and file upload


Draw Dots
Draw Ties
Draw Tuplets
Inhouse: Refactor parameters of (1pd)
createInstrumentBracket (upper, lower stave)
createGroupBracket (upper, lower stave)
Draw Articulations
Draw Grace notes
Draw In-Staff Clef
Draw Instrument Braces
Draw Group Brackets
Inhouse: Tuplet label placement (1pd)
Inhouse: Stem Direction calculator (2pd)
Inhouse: Convert SkyBottomLineCalculator (5pd)
adapt y-layout code
Draw Measure numbers
Draw Chord Symbols
Draw Repetitions
Words
Endings
Lines
Inhouse: Refactor for Slur Handling (2pd)
Draw Slurs
Draw Word Expressions
Dynamics
Tempo
Other
Draw Wedges
Draw Lyrics
Words
Connecting dashes
continuing underscores
Draw Ornaments

Tabs?
