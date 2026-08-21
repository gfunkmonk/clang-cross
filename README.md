# $\Huge{\color{#f5750e}{clang-cross}}$       [![Release](https://github.com/gfunkmonk/clang-cross/actions/workflows/release.yaml/badge.svg?branch=main)](https://github.com/gfunkmonk/clang-cross/actions/workflows/release.yaml)

$\large{\textbf{\color{#7FFF00}{This is a simple, lightweight project for making cross-compilation toolchain with clang and either GNU or MUSL libc.}}}$  

Run `./scripts/make list` to print the up-to-date set of targets directly from `targets/`.
=======
#
                                                  
|   $$\huge{\color{#DF73FF}MUSL LIBC}$$           |            |           |          |   |   |       $$\huge{\color{#6CB4EE}GLIBC GNU}$$       |            |           |          |
|:------------------------------:|------------|-----------|----------|---|---|:-----------------------------:|------------|-----------|----------|
|                                |            |           |          |   |   |                               |            |           |          |
|            **Target**            | **Kernel** | **Clang** | **Musl** |   |   | **Target**                      | **Kernel** | **Clang** | **Libc** |
|   aarch64-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | aarch64-unknown-linux-gnu     |            |   22.1.6  |   2.44   |
|  aarch64_be-unknown-linux-musl |   6.18.41  |   22.1.6  |   1.2.6  |   |   | aarch64_be-unknown-linux-gnu  |   6.18.41  |   22.1.6  |   2.44   |
|   arm-unknown-linux-musleabi   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | alphaev56-unknown-linux-gnu   |   6.18.41  |   22.1.6  |   2.44   |
|  arm-unknown-linux-musleabihf  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | alphaev67-unknown-linux-gnu   |   6.18.41  |   22.1.6  |   2.44   |
|  armv5-unknown-linux-musleabi  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | arm-unknown-linux-gnueabi     |   6.18.41  |   22.1.6  |   2.44   |
|  armv6-unknown-linux-musleabi  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | arm-unknown-linux-gnueabihf   |   6.18.41  |   22.1.6  |   2.44   |
| armv6-unknown-linux-musleabihf |   6.18.41  |   22.1.6  |   1.2.6  |   |   | armv4t-unknown-linux-gnueabi  |   6.18.41  |   22.1.6  |   2.44   |
|  armv7-unknown-linux-musleabi  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | armv5-unknown-linux-gnueabi   |   6.18.41  |   22.1.6  |   2.44   |
| armv7-unknown-linux-musleabihf |   6.18.41  |   22.1.6  |   1.2.6  |   |   | armv6-unknown-linux-gnueabi   |   6.18.41  |   22.1.6  |   2.44   |
|     i386-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | armv6-unknown-linux-gnueabihf |   6.18.41  |   22.1.6  |   2.44   |
|     i486-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | armv7-unknown-linux-gnueabi   |   6.18.41  |   22.1.6  |   2.44   |
|     i586-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | armv7-unknown-linux-gnueabihf |   6.18.41  |   22.1.6  |   2.44   |
|     i686-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | hppa-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
| loongarch64-unknown-linux-musl |   6.18.41  |   22.1.6  |   1.2.6  |   |   | i386-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|     m68k-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | i486-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|  microblaze-xilinx-linux-musl  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | i586-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
| microblazeel-xilinx-linux-musl |   6.18.41  |   22.1.6  |   1.2.6  |   |   | i686-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|     mips-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | loongarch64-unknown-linux-gnu |   6.18.41  |   22.1.6  |   2.44   |
|    mips-unknown-linux-muslsf   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | m68k-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|    mips64-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | microblaze-xilinx-linux-gnu   |   6.18.41  |   22.1.6  |   2.44   |
|   mips64el-unknown-linux-musl  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | microblazeel-xilinx-linux-gnu |   6.18.41  |   22.1.6  |   2.44   |
|    mipsel-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | mips-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|   mipsel-unknown-linux-muslsf  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | mips-unknown-linux-gnusf      |   6.18.41  |   22.1.6  |   2.44   |
|     or1k-unknown-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | mips64-unknown-linux-gnu      |   6.18.41  |   22.1.6  |   2.44   |
|   powerpc-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | mips64el-unknown-linux-gnu    |   6.18.41  |   22.1.6  |   2.44   |
|  powerpc-unknown-linux-muslsf  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | mipsel-unknown-linux-gnu      |   6.18.41  |   22.1.6  |   2.44   |
|  powerpc64-unknown-linux-musl  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | mipsel-unknown-linux-gnusf    |   6.18.41  |   22.1.6  |   2.44   |
| powerpc64le-unknown-linux-musl |   6.18.41  |   22.1.6  |   1.2.6  |   |   | or1k-unknown-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|  powerpcle-unknown-linux-musl  |   6.18.41  |   22.1.6  |   1.2.6  |   |   | powerpc-unknown-linux-gnu     |   6.18.41  |   22.1.6  |   2.44   |
| powerpcle-unknown-linux-muslsf |   6.18.41  |   22.1.6  |   1.2.6  |   |   | powerpc-unknown-linux-gnusf   |   6.18.41  |   22.1.6  |   2.44   |
|   riscv32-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | powerpc64-unknown-linux-gnu   |   6.18.41  |   22.1.6  |   2.44   |
|   riscv64-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | powerpc64le-unknown-linux-gnu |   6.18.41  |   22.1.6  |   2.44   |
|      s390x-ibm-linux-musl      |   6.18.41  |   22.1.6  |   1.2.6  |   |   | powerpcle-unknown-linux-gnu   |   6.18.41  |   22.1.6  |   2.44   |
|     sh4-multilib-linux-musl    |   6.18.41  |   22.1.6  |   1.2.6  |   |   | powerpcle-unknown-linux-gnusf |   6.18.41  |   22.1.6  |   2.44   |
|    x86_64-unknown-linux-musl   |   6.18.41  |   22.1.6  |   1.2.6  |   |   | riscv32-unknown-linux-gnu     |   6.18.41  |   22.1.6  |   2.44   |
|                                |            |           |          |   |   | riscv64-unknown-linux-gnu     |   6.18.41  |   22.1.6  |   2.44   |
|                                |            |           |          |   |   | s390x-ibm-linux-gnu           |   6.18.41  |   22.1.6  |   2.44   |
|                                |            |           |          |   |   | sh4-multilib-linux-gnu        |   6.18.41  |   22.1.6  |   2.44   |
|                                |            |           |          |   |   | sparc-unknown-linux-gnu       |   6.18.41  |   22.1.6  |   2.44   |
|                                |            |           |          |   |   | sparc64-unknown-linux-gnu     |   6.18.41  |   22.1.6  |   2.44   |
|                                |            |           |          |   |   | x86_64-unknown-linux-gnu      |   6.18.41  |   22.1.6  |   2.44   |Run `./scripts/make list` to print the up-to-date set of targets directly from `targets/`.

## How to use

Download the tarball from the [release page](https://github.com/gfunkmonk/clang-cross/releases) and extract it to `/opt/x-tools`:

```sh
sudo mkdir -p /opt/x-tools
sudo tar -xf ${target}.tar.xz -C /opt/x-tools
```

## How to build

Fork this project and create a new release, or build manually:

```sh
./scripts/make ${target}
```

## License

MIT

## Acknowledgements

We would like to express our gratitude to the following individuals and projects:

- [llvm](https://llvm.org)
- [linux](https://kernel.org)
- [glibc](https://www.gnu.org/software/libc)
- [musl](https://www.musl-libc.org)
