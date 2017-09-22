---
title: Setting up OSMD for Development
layout: page
permalink: "/develop/setup/"
lang: en_US
---

This page describes how to set up OpenSheetMusicDisplay for development.

## Clone source
```sh
# Clone the repository from Github
$ git clone git@github.com:opensheetmusicdisplay/opensheetmusicdisplay.git
```

## Install Grunt
> As of today, OSMD requires Grunt for build tasks. This is going to change in the future, since all OSMD build tasks will be moved to npm scripts.

Install Grunt globally:
```sh
$ npm install -g grunt-cli
```

## Install dependencies
This requires `npm` to be installed.
```sh
$ npm install
```

## Build
```sh
$ grunt build:demo # Builds the demo
$ grunt build:test # Builds the tests
$ grunt build:dist # Builds for distribution on npm and Bower
```
All bundled build artifacts will be placed in `build/`. The compiled ES module will be located at `dist/`.
