# clang-cross

This is a simple, lightweight project for making cross-compilation toolchain with clang and {gnu, musl} libc.

## Supported targets

| Target                         | Kernel  | Clang  | Libc   |
|--------------------------------|---------|--------|--------|
| aarch64-unknown-linux-musl     | 6.18.22 | 21.1.8 | 1.2.6  |
| arm-unknown-linux-musleabi     | 6.18.22 | 21.1.8 | 1.2.6  |
| arm-unknown-linux-musleabihf   | 6.18.22 | 21.1.8 | 1.2.6  |
| armv7-unknown-linux-musleabi   | 6.18.22 | 21.1.8 | 1.2.6  |
| armv7-unknown-linux-musleabihf | 6.18.22 | 21.1.8 | 1.2.6  |
| i586-unknown-linux-musl        | 6.18.22 | 21.1.8 | 1.2.6  |
| i686-unknown-linux-musl        | 6.18.22 | 21.1.8 | 1.2.6  |
| loongarch64-unknown-linux-musl | 6.18.22 | 21.1.8 | 1.2.6  |
| mips64el-unknown-linux-musl    | 6.18.22 | 21.1.8 | 1.2.6  |
| mips64-unknown-linux-musl      | 6.18.22 | 21.1.8 | 1.2.6  |
| mipsel-unknown-linux-musl      | 6.18.22 | 21.1.8 | 1.2.6  |
| mipsel-unknown-linux-muslsf    | 6.18.22 | 21.1.8 | 1.2.6  |
| mips-unknown-linux-musl        | 6.18.22 | 21.1.8 | 1.2.6  |
| mips-unknown-linux-muslsf      | 6.18.22 | 21.1.8 | 1.2.6  |
| powerpc64le-unknown-linux-musl | 6.18.22 | 21.1.8 | 1.2.6  |
| powerpc64-unknown-linux-musl   | 6.18.22 | 21.1.8 | 1.2.6  |
| powerpcle-unknown-linux-musl   | 6.18.22 | 21.1.8 | 1.2.6  |
| powerpc-unknown-linux-musl     | 6.18.22 | 21.1.8 | 1.2.6  |
| riscv32-unknown-linux-musl     | 6.18.22 | 21.1.8 | 1.2.6  |
| riscv64-unknown-linux-musl     | 6.18.22 | 21.1.8 | 1.2.6  |
| s390x-ibm-linux-musl           | 6.18.22 | 21.1.8 | 1.2.6  |
| x86_64-unknown-linux-musl      | 6.18.22 | 21.1.8 | 1.2.6  |

## How to use

Download the tarball from the [release page](https://github.com/cross-tools/clang-cross/releases) and extract it to `/opt/x-tools`:

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
