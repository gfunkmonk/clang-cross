# clang-cross

This is a simple, lightweight project for making cross-compilation toolchain with clang and {gnu, musl} libc.

## Supported targets

### musl targets

| Target                           | Kernel  | Clang  | Libc   |
|----------------------------------|---------|--------|--------|
| aarch64-unknown-linux-musl       | 6.18.23 | 22.1.0 | 1.2.6  |
| aarch64_be-unknown-linux-musl    | 6.18.23 | 22.1.0 | 1.2.6  |
| arm-unknown-linux-musleabi       | 6.18.23 | 22.1.0 | 1.2.6  |
| arm-unknown-linux-musleabihf     | 6.18.23 | 22.1.0 | 1.2.6  |
| armv5-unknown-linux-musleabi     | 6.18.23 | 22.1.0 | 1.2.6  |
| armv6-unknown-linux-musleabi     | 6.18.23 | 22.1.0 | 1.2.6  |
| armv6-unknown-linux-musleabihf   | 6.18.23 | 22.1.0 | 1.2.6  |
| armv7-unknown-linux-musleabi     | 6.18.23 | 22.1.0 | 1.2.6  |
| armv7-unknown-linux-musleabihf   | 6.18.23 | 22.1.0 | 1.2.6  |
| i386-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| i486-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| i586-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| i686-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| loongarch64-unknown-linux-musl   | 6.18.23 | 22.1.0 | 1.2.6  |
| m68k-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| microblaze-xilinx-linux-musl     | 6.18.23 | 22.1.0 | 1.2.6  |
| microblazeel-xilinx-linux-musl   | 6.18.23 | 22.1.0 | 1.2.6  |
| mips-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| mips-unknown-linux-muslsf        | 6.18.23 | 22.1.0 | 1.2.6  |
| mips64-unknown-linux-musl        | 6.18.23 | 22.1.0 | 1.2.6  |
| mips64el-unknown-linux-musl      | 6.18.23 | 22.1.0 | 1.2.6  |
| mipsel-unknown-linux-musl        | 6.18.23 | 22.1.0 | 1.2.6  |
| mipsel-unknown-linux-muslsf      | 6.18.23 | 22.1.0 | 1.2.6  |
| or1k-unknown-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| powerpc-unknown-linux-musl       | 6.18.23 | 22.1.0 | 1.2.6  |
| powerpc-unknown-linux-muslsf     | 6.18.23 | 22.1.0 | 1.2.6  |
| powerpc64-unknown-linux-musl     | 6.18.23 | 22.1.0 | 1.2.6  |
| powerpc64le-unknown-linux-musl   | 6.18.23 | 22.1.0 | 1.2.6  |
| powerpcle-unknown-linux-musl     | 6.18.23 | 22.1.0 | 1.2.6  |
| powerpcle-unknown-linux-muslsf   | 6.18.23 | 22.1.0 | 1.2.6  |
| riscv32-unknown-linux-musl       | 6.18.23 | 22.1.0 | 1.2.6  |
| riscv64-unknown-linux-musl       | 6.18.23 | 22.1.0 | 1.2.6  |
| s390x-ibm-linux-musl             | 6.18.23 | 22.1.0 | 1.2.6  |
| sh4-multilib-linux-musl          | 6.18.23 | 22.1.0 | 1.2.6  |
| x86_64-unknown-linux-musl        | 6.18.23 | 22.1.0 | 1.2.6  |

### gnu (glibc) targets

| Target                           | Kernel  | Clang  | Libc   |
|----------------------------------|---------|--------|--------|
| aarch64-unknown-linux-gnu        | 6.18.23 | 22.1.0 | 2.43   |
| aarch64_be-unknown-linux-gnu     | 6.18.23 | 22.1.0 | 2.43   |
| alphaev56-unknown-linux-gnu      | 6.18.23 | 22.1.0 | 2.43   |
| alphaev67-unknown-linux-gnu      | 6.18.23 | 22.1.0 | 2.43   |
| arm-unknown-linux-gnueabi        | 6.18.23 | 22.1.0 | 2.43   |
| arm-unknown-linux-gnueabihf      | 6.18.23 | 22.1.0 | 2.43   |
| armv4t-unknown-linux-gnueabi     | 6.18.23 | 22.1.0 | 2.43   |
| armv5-unknown-linux-gnueabi      | 6.18.23 | 22.1.0 | 2.43   |
| armv6-unknown-linux-gnueabi      | 6.18.23 | 22.1.0 | 2.43   |
| armv6-unknown-linux-gnueabihf    | 6.18.23 | 22.1.0 | 2.43   |
| armv7-unknown-linux-gnueabi      | 6.18.23 | 22.1.0 | 2.43   |
| armv7-unknown-linux-gnueabihf    | 6.18.23 | 22.1.0 | 2.43   |
| hppa-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| i386-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| i486-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| i586-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| i686-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| loongarch64-unknown-linux-gnu    | 6.18.23 | 22.1.0 | 2.43   |
| m68k-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| microblaze-xilinx-linux-gnu      | 6.18.23 | 22.1.0 | 2.43   |
| microblazeel-xilinx-linux-gnu    | 6.18.23 | 22.1.0 | 2.43   |
| mips-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| mips-unknown-linux-gnusf         | 6.18.23 | 22.1.0 | 2.43   |
| mips64-unknown-linux-gnu         | 6.18.23 | 22.1.0 | 2.43   |
| mips64el-unknown-linux-gnu       | 6.18.23 | 22.1.0 | 2.43   |
| mipsel-unknown-linux-gnu         | 6.18.23 | 22.1.0 | 2.43   |
| mipsel-unknown-linux-gnusf       | 6.18.23 | 22.1.0 | 2.43   |
| or1k-unknown-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| powerpc-unknown-linux-gnu        | 6.18.23 | 22.1.0 | 2.43   |
| powerpc-unknown-linux-gnusf      | 6.18.23 | 22.1.0 | 2.43   |
| powerpc64-unknown-linux-gnu      | 6.18.23 | 22.1.0 | 2.43   |
| powerpc64le-unknown-linux-gnu    | 6.18.23 | 22.1.0 | 2.43   |
| powerpcle-unknown-linux-gnu      | 6.18.23 | 22.1.0 | 2.43   |
| powerpcle-unknown-linux-gnusf    | 6.18.23 | 22.1.0 | 2.43   |
| riscv32-unknown-linux-gnu        | 6.18.23 | 22.1.0 | 2.43   |
| riscv64-unknown-linux-gnu        | 6.18.23 | 22.1.0 | 2.43   |
| s390x-ibm-linux-gnu              | 6.18.23 | 22.1.0 | 2.43   |
| sh4-multilib-linux-gnu           | 6.18.23 | 22.1.0 | 2.43   |
| sparc-unknown-linux-gnu          | 6.18.23 | 22.1.0 | 2.43   |
| sparc64-unknown-linux-gnu        | 6.18.23 | 22.1.0 | 2.43   |
| x86_64-unknown-linux-gnu         | 6.18.23 | 22.1.0 | 2.43   |

Run `./scripts/make list` to print the up-to-date set of targets directly from `targets/`.

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
