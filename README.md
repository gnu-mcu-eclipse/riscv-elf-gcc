## GNU MCU Eclipse RISC-V Embedded GCC binaries

This xPack installs the platform specific binaries for the RISC-V Embedded toolchain.

This project is open source and it is publicly available from GitHub [gnu-mcu-eclipse/riscv-none-gcc-xpack](https://github.com/gnu-mcu-eclipse/riscv-none-gcc-xpack).

## Prerequisites

A recent [Node.js](https://nodejs.org) (>7.x), since the ECMAScript 6 class syntax is used.

If this is your first encounter with `npm`, you need to install the [node.js](https://nodejs.org/) JavScript run-time. The process is straightforward and does not pollute the system locations significantly; just pick the current version, download the package suitable for your platform and install it as usual. The result is a binary program called `node` that can be used to execute JavaScript code from the terminal, and a link called `npm`, pointing to the `npm-cli.js` script, which is part of the node module that implements the npm functionality. On Windows, it is recommended to first install the [Git for Windows](https://git-scm.com/download/win) package.

With `npm` available, the next step is to install `xpm`, the xPack package manager:

```console
$ sudo npm install xpm --global
```

On Windows, global `npm` packages are installed in the user home folder, and do not require `sudo`.

## Easy install

The module is available as [**gnu-mcu-eclipse/riscv-none-gcc**](https://www.npmjs.com/package/gnu-mcu-eclipse/riscv-none-gcc) from the public repository; with `npm` already available, installing `xsvd` is quite easy:

```console
$ xpm install @gnu-mcu-eclipse/riscv-none-gcc --global
```

Global `xpm` packages are installed in the user home folder, and do not require `sudo`.

To remove the installed xPack, the command is similar:

```console
$ xpm uninstall @gnu-mcu-eclipse/riscv-none-gcc --global
```

(Note: not yet implemented)

## Developer info

### Git repo

```console
$ git clone https://github.com/nu-mcu-eclipse/riscv-none-gcc-xpack.git riscv-none-gcc-xpack.git
```

### Toolchain binaries

The binaries are downloaded from the [gnu-mcu-eclipse/riscv-none-gcc](https://github.com/gnu-mcu-eclipse/riscv-none-gcc) [releases](https://github.com/gnu-mcu-eclipse/riscv-none-gcc/releases).

### Standard compliance

The module uses ECMAScript 6 class definitions.

As style, it uses the [JavaScript Standard Style](https://standardjs.com/), automatically checked at each commit via Travis CI.

Known and accepted exceptions:

- none.

To manually fix compliance with the style guide (where possible):

```console
$ npm run fix

> @gnu-mcu-eclipse/riscv-none-gcc@0.1.0 fix .../GNU MCU Eclipse/xpacks/riscv-none-gcc-xpack.git
> standard --fix
```

### Documentation metadata

The documentation metadata follows the [JSdoc](http://usejsdoc.org) tags.

To enforce checking at file level, add the following comments right after the `use strict`:

```js
'use strict'
/* eslint valid-jsdoc: "error" */
/* eslint max-len: [ "error", 80, { "ignoreUrls": true } ] */
```

Note: be sure C style comments are used, C++ styles are not parsed by [ESLint](http://eslint.org).

### How to publish

* commit all changes
* `npm run test` (`fix` included)
* update `CHANGELOG.md`; commit with a message like _prepare v0.1.2_
* `npm version patch`
* push all changes to GitHub; this should trigger CI
* wait for CI tests to complete
* `npm publish`

## License

The original content is released under the [MIT License](https://opensource.org/licenses/MIT), with
all rights reserved to Liviu Ionescu.
