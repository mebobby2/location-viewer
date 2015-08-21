# Location Viewer

This is for me to play with the React.js framework.

The recommended way to write React code is using JSX, a JavaScript extension. You then must transform the JSX code into JavaScript.
Reactify, which is a Browserify transform, is a tool that can be used to do this. Because Reactify is a Browserify transform,
it automatically comes with all the other goodies that Browserify offers, such as getting access to the require() node.js call
and with it the ability to install and use libraries from npm.

## Development setup
- npm to install the dependencies
- run while developing: node_modules/.bin/watchify -v -d -t [ reactify --es6 ] main.js -o compiled.js
  Watchify will monitor your files and recompile your source code if needed. The compiled file is compiled.js 

## Production ready
- Once you are happy with your code, run: NODE_ENV=production node_modules/.bin/browserify -t [ reactify --es6 ] main.js | node_modules/.bin/uglifyjs > compiled.min.js
  This create minified compile which you can use in production.
