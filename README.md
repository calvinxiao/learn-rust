# Rust

## 十大人物

- Katharina Fey https://twitter.com/spacekookie
- 原作者 https://twitter.com/nikomatsakis

## 十大 github repo

- https://github.com/brson/rust-anthology
- https://github.com/rust-lang/rfcs
- https://github.com/rust-random/rand



## 十大网站

- https://www.rust-lang.org/
- https://brson.github.io/rust-anthology/1/index.html
- https://www.youtube.com/channel/UCaYhcUwRBNscFNUKTjgPFiA/videos
- 

## 书籍

- 圣经 https://doc.rust-lang.org/book/
- 东哥的《Rust 编程之道》https://item.jd.com/12479415.html



## Bible 读书笔记



> 21 章节, *by Steve Klabnik and Carol Nichols*



### 0x01 Getting Started

脚本安装太慢，最后去官网下载了 pkg 包

`println!` 但是 Rust macro

Cargo! Cargo!

Rustaceans, Rubyists, Gophers

`cargo new hello_cargo`

toml, this another markup language, haha

`cargo build && tree`

```bash
$ cargo help
Some common cargo commands are (see all commands with --list):
    build       Compile the current package
    check       Analyze the current package and report errors, but don't build object files
    clean       Remove the target directory
    doc         Build this package's and its dependencies' documentation
    new         Create a new cargo package
    init        Create a new cargo package in an existing directory
    run         Run a binary or example of the local package
    test        Run the tests
    bench       Run the benchmarks
    update      Update dependencies listed in Cargo.lock
    search      Search registry for crates
    publish     Package and upload this package to the registry
    install     Install a Rust binary. Default location is $HOME/.cargo/bin
    uninstall   Uninstall a Rust binary
```

`cargo build --release`

### 0x02 猜猜猜

> You’ll learn about `let`, `match`, methods, associated functions, using external crates, and more! 

https://doc.rust-lang.org/std/prelude/index.html, prelude, pre-include?

let, let, let, lisp, lisp, lisp

>  In Rust, variables are immutable by default

```rust
let a = 1;
let mut b = 2;
```

associated function, class methods?

error is expected.

加速加速加速

```bash
# vim ~/.cargo/config
[source.crates-io]
registry = "https://github.com/rust-lang/crates.io-index"
replace-with = 'ustc'
[source.ustc]
registry = "git://mirrors.ustc.edu.cn/crates.io-index"
```

`cargo doc --open` 厉害

TODO 学习 rand 库

`let's match!`

