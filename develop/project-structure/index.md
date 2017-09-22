---
layout: page
title: Project Structure
permalink: /develop/project-structure/
lang: en_US
---

## Project Structure
### Sources
* **src** source code
* **test** contains code and resources for tests. This directory mirrors the structure of the **src** folder. Files containing test suites, end with a `_Test` suffix.
    * **data** contains sample MusicXML files
* **demo** contains the sources for the demo page (will be moved inside **src** soon, see [#104](https://github.com/opensheetmusicdisplay/opensheetmusicdisplay/issues/104))

### Build Artifacts
After insatlling and building OSMD, the following directories conatining build artifacts may appear:
* **node_modules** contains the npm packages which OSMD depends on
* **build** contains build outputs, like the bundled and minified JavaScript, class documentation and demo
* **dist** contains the transpiled JavaScript that will be shipped with the npm bundle

## Structure of the source code
* **Common**
    * **DataObjects** contains basic data objects like fractions, points, rectangles, colours etc.
    * **Enums** contains constants for fonts and text styles
    * **FileIO** contains code for handling `.xml` and .`mxl` files
    * **Logging.ts** OSMD's logging framework
* **MusicalScore**
    * **Graphical** contains definitions of *graphical* objects
      * **VexFlow** VexFlow implementation of OSMD's graphical objects
      * **GraphicalNote** is the graphical counterpart of a `Note`
      * **Measure** is the graphical counterpart of a `SourceMeasure`
      * **GraphicalMusicSheet** is the graphical counterpart of a `MusicSheet`
      * **MusicSheetCalculator** takes a `MusicSheet` and populates a `GraphicalMusicSheet`
      * **MusicSheetDrawer** draws a `GraphicalMusicSheet`
      * **MusicSystem** represents a "row" in a music sheet, which includes all instruments and measures until a new line
      * **StaffEntry** is the graphical counterpart of a `SourceStaffEntry`
      * tdb
    * **Interfaces** contains interface classes for graphical symbols, text display and other, which are then implemented with VexFlow methods
    * **MusicParts** provides iteration through the music sheet (will handle repetitions too)
    * **MusicSource**
      * tdb
    * **ScoreIO**
      * `InstrumentReader.ts`
      * `MusicSheetReader.ts`
      * `VoiceGenerator.ts`
    * **VoiceData** contains definitions of "source" objects
      * **Expressions** like crescendo, style of playing etc.
      * **Instructions** like clef signatures, key signatures, time signatures and repeats
    * **Exceptions.ts** for errors in reading the music sheet
    * **MusicSheet.ts** logical representation of music sheets: title and other metadata, page width, instruments, measures etc.
* **OSMD**
    * **OSMD.ts** contains the API for OSMD
    * **Cursor.ts** implements the cursor iterating the music sheet
    * **AJAX.ts** provides support for loading sheet music by URL
    * **ResizeHandler.ts** implements the automatic resizing when window size changes
* **Util** contains methods to operate on arrays, or wrappers to basic Maths functions
