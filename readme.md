# repl-it

Creates a repl in the current directory with all the packages listed in `devDependencies` and `dependencies` loaded into the local context. Uses pkginfo to determine the root of your project.

## io.js REPL features
* Command line history -- If you're using io.js version 1 or higher you have access to persistant command-line history (enabled by default).  To disable use `--no-history`.
* "MAGIC" mode -- If you're in io.js 2 or higher, defaults to magic, which will automatically run "strict mode only" statements in strict mode. To disable use `--no-magic`.


## Usage

```
~/src/awesome-node-project> cat package.json
{
  "name": "repl-it",
  "version": "1.0.1",
  "description": "Loads all the packages in your package.json and creates a repl for you",
  "main": "index.js",
  "scripts": {
    "test": "tap test/*spec.js"
  },
  "bin": {
    "repl-it": "./index.js"
  },
  "repository": {
    "type": "git",
    "url": "git://github.com/toddself/repl-it"
  },
  "keywords": [
    "repl"
  ],
  "author": "Todd Kennedy <todd@selfassembled.org>",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/toddself/repl-it/issues"
  },
  "homepage": "https://github.com/toddself/repl-it",
  "dependencies": {
    "camel-case": "^1.0.2",
    "pkginfo": "^0.3.0",
    "xtend": "^4.0.0"
  }
}
~/src/repl-it> repl-it
repl-it> typeof xtend
'function'
repl-it> typeof camelCase
'function'
repl-it> ^D
~/src/repl-it> cd test
~/src/repl-it/test> repl-it
repl-it> typeof camelCase
'function'
```

Packages are automatically camelcased for you.
```
~/src/awesome-node-project> repl-it
repl-it> typeof camelCase
'function'
repl-it>
```

# Installation

`npm i -g repl-it`

# Tests

None yet.  Probably not ever.  Eh.

# Contributors

* Eugene Sharygin ([eush77](https://github.com/eush77))
* Evan Senter ([evansenter](https://github.com/evansenter))

# License

MIT. © 2014 Todd Kennedy