# ish [![Build Status](https://travis-ci.org/nickb1080/ish.svg?branch=master)](https://travis-ci.org/nickb1080/ish)

Install it globally

```
npm i -g ish
```

Choose some files, run them, and inject their `module.exports` properties into the global scope of a new REPL.

There are probably some lingering edge cases around properly resolving file paths depending on whether the caller is `bin/ish` or another script.


Given a file with CommonJS exports...
```
// my-module.js
var x = "some value";
```

Then, from the command line...
```
> ish myModule=./my-module.js

$ console.log(myModule)
"some value"
```
