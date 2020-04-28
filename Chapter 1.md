# Copy of 1: Getting Started

[https://doc.rust-lang.org/book/ch01-00-getting-started.html](https://doc.rust-lang.org/book/ch01-00-getting-started.html)

## Alternate Mac Install Guide

Assumes you have [brew]([https://brew.sh](https://brew.sh/)) already installed

```bash
$ brew install rustup 
$ rustup-init # better than `brew install rust`
```

`rustup` === `nvm`
(you may need to use a fresh terminal after setup) [or `source` your shell's profile]

```bash
$ cargo --version # or -V
```

Macro ≠ Function... reasons in Ch. 19 😃

Rust is an ahead-of-time compiled language, meaning you can compile a program and give the executable to someone else, and they can run it even without having Rust installed. ****Good to see a first usage of *Rustaceans*. 😃

"There’s a place for everything, and everything is in its place."