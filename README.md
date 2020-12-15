<h1 align="center">
  <code>polyfuse</code>
</h1>

<div align="center">
  <strong>
    A FUSE (Filesystem in Userspace) library for Rust.
  </strong>
</div>

<br />

<div align="center">
  <a href="https://crates.io/crates/polyfuse">
    <img src="https://img.shields.io/crates/v/polyfuse.svg?style=flat-square"
         alt="crates.io"
    />
  </a>
  <a href="https://blog.rust-lang.org/2020/11/19/Rust-1.48.html">
    <img src="https://img.shields.io/badge/minimum%20rustc-1.48.0-yellowgreen?style=flat-square"
         alt="rust toolchain"
    />
  </a>
  <a href="https://docs.rs/polyfuse">
    <img src="https://img.shields.io/badge/docs-latest-blue.svg?style=flat-square"
         alt="docs.rs" />
  </a>
  <a href="https://discord.gg/qHHdweYFVp">
    <img src="https://img.shields.io/discord/778686351352135701.svg?style=flat-square&label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2"
         alt="Discord channel"
    />
  </a>
</div>

<br />

`polyfuse` is a library for implementing filesystems based on [Filesystem in Userspace (FUSE)](https://en.wikipedia.org/wiki/Filesystem_in_Userspace) in Rust.

The goal of this project is to provide a Rust FUSE library that has a high affinity with the `async`/`.await` syntax stabilized in Rust 1.39.

## Platform Requirements

Currently, `polyfuse` only supports the Linux platforms with the FUSE ABI version is 7.23 or higher.
The required kernel version is Linux 3.15 or later.

> Adding support for other Unix platform running FUSE (FreeBSD, macOS, and so on) is a future work.

In order to establish the connection with the FUSE kernel driver, the command
`fusermount` must be installed on the platform where the filesystem runs.
This binary is typically including in the fuse package provided by the distribution's package system.

On Debian/Ubuntu or other APT based distributions:

```shell-session
$ sudo apt-get install fuse
```

On Fedora/RHEL or other RPM based distributions:

```shell-session
$ sudo dnf install fuse
```

On Arch Linux or other Pacman based distributions:

```shell-session
$ sudo pacman -S fuse2
```

## Resources

* [Examples](https://github.com/ubnt-intrepid/polyfuse/tree/master/examples)
* [API documentation (docs.rs)](https://docs.rs/polyfuse)
* [API documentation (master)](https://ubnt-intrepid.github.io/polyfuse/)

## License

This library is licensed under either of

* MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)
* Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)

at your option.
