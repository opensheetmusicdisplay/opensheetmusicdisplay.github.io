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

## Install dependencies
This requires `npm` to be installed.
```sh
$ npm install
```

## Build
```sh
$ npm start # Build and run demo (served on localhost:8000)
$ npm run test # Builds the tests
$ npm run build # Builds for distribution on npm and Bower
```
All bundled build artifacts will be placed in `build/`.
