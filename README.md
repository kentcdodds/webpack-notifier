# webpack-notifier

[![Build Status](https://img.shields.io/travis/Turbo87/webpack-notifier.svg)](https://travis-ci.org/Turbo87/webpack-notifier)
[![npm Version](https://img.shields.io/npm/v/webpack-notifier.svg)](https://www.npmjs.com/package/webpack-notifier)

This is a [webpack](http://webpack.github.io/) plugin that uses the
[node-notifier](https://github.com/mikaelbr/node-notifier) package to
display build status system notifications to the user.

![webpack-notifier screenshot](screenshot.png)

> This is a fork of the
[webpack-error-notification](https://github.com/vsolovyov/webpack-error-notification)
plugin. It adds support for Windows and there is no need to manually install
the `terminal-notifier` package on OS X anymore.

The plugin will notify you about the first run (success/fail),
all failed runs and the first successful run after recovering from
a build failure. In other words: it will stay silent if everything
is fine with your build.


## Installation

Use `npm` to install this package:

    npm install --save-dev webpack-error-notification

Check the `node-notifier`
[Requirements](https://github.com/mikaelbr/node-notifier#requirements)
whether you need to install any additional tools for your OS.


## Usage

In the `webpack.config.js` file:

```js
var WebpackNotifierPlugin = require('webpack-notifier');

// ...

module: {
  plugins: [
    new WebpackNotifierPlugin(),
  ]
},

// ...
```
