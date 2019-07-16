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

`println!` 是 Rust macro

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

### 0x03 [Common Programming Concepts](https://doc.rust-lang.org/book/ch03-00-common-programming-concepts.html#common-programming-concepts)

出去看了下 [「RustConAsia 2019」如何高效学习Rust](https://zhuanlan.zhihu.com/p/63232238)

Rust 一个特点就是编译器会找出变量可变性错误的使用，并发ownership 误用等情况，一般来说，能编译，跑起来也不会有问题了

cosnt must be with type, MAX_POINTS

shadowing 允许改变变量类型, mut 只能改变值

有 `i128` 和 `u128`

`let (x, y, z) = tup;` pattern matching

tup.1 tup.2 tup.3

array 内存分配到 stack

function  命名用 snake case

statement 和 expression 分开，`1 + 1` 是 expression，`let a = 1 + 1` 是 statement

loop, while, for

### 0x04 Ownership

- Each value in Rust has a variable that’s called its *owner*.
- There can only be one owner at a time.
- When the owner goes out of scope, the value will be dropped.



- At any given time, you can have *either* one mutable reference *or* any number of immutable references.
- References must always be valid.



### 0x05 Structs

```rust
fn build_user(email: String, username: String) -> User {
    User {
        email,
        username,
        active: true,
        sign_in_count: 1,
    }
}
```

javascript, javascript, javascript...

```
let user2 = User {
    email: String::from("another@example.com"),
    username: String::from("anotherusername567"),
    ..user1
};
```

cannot be partial mutable

WTF is lifetime
