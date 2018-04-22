[![npm (scoped)](https://img.shields.io/npm/v/@gnu-mcu-eclipse/riscv-none-gcc.svg)](https://www.npmjs.com/package/@gnu-mcu-eclipse/riscv-none-gcc) 
[![license](https://img.shields.io/github/license/gnu-mcu-eclipse/riscv-none-gcc-xpack.svg)](https://github.com/gnu-mcu-eclipse/riscv-none-gcc-xpack/blob/xpack/LICENSE) 
[![Standard](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com/)


## GNU MCU Eclipse RISC-V Embedded GCC binaries

This xPack installs the platform specific binaries for the RISC-V Embedded toolchain.

This project is open source and it is publicly available from [GitHub](https://github.com/gnu-mcu-eclipse/riscv-none-gcc-xpack).

## How to use

This section is intended for developers who plan to use the RISC-V Embedded GCC toolchain.

### Prerequisites

A recent [`xpm`](https://www.npmjs.com/package/xpm), which is a 
portable [Node.js](https://nodejs.org/) command line application.

## Easy install

The module is available as [`@gnu-mcu-eclipse/riscv-none-gcc`](https://www.npmjs.com/package/gnu-mcu-eclipse/riscv-none-gcc) from the `npmjs.com` registry; with `xpm` available, installing the latest version of the package is quite easy:

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
$ git clone https://github.com/gnu-mcu-eclipse/riscv-none-gcc-xpack.git riscv-none-gcc-xpack.git
```

### Toolchain binaries

The binaries are downloaded from the [gnu-mcu-eclipse/riscv-none-gcc](https://github.com/gnu-mcu-eclipse/riscv-none-gcc) [releases](https://github.com/gnu-mcu-eclipse/riscv-none-gcc/releases) project.

### Code standard compliance

The module currently does not include any JavaScript code.

### Code documentation metadata

The module currently does not include any documentation metadata

## Maintainer info

### How to publish

* open [releases](https://github.com/gnu-mcu-eclipse/riscv-none-gcc/releases) and select the latest release
* update the `baseUrl:` with the file URLs (including the tag/version)
* from the blog post, copy the SHA & file names
* commit all changes, use a message like `7.2.0-1.2` (without `v`)
* `npm version 7.2.0-1.2`
* push all changes to GitHub
* `npm publish`

## License

The original content is released under the [MIT License](https://opensource.org/licenses/MIT), with all rights reserved to [Liviu Ionescu](https://github.com/ilg-ul).
