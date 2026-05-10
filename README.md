# Rust Learning Roadmap

A prioritised guide to learning Rust — from most to least important.

---

## Phase 1 — The Rust Fundamentals
> Start here. Everyone needs this.

### 🔐 Ownership & Borrowing *(Critical)*
The #1 thing that makes Rust unique. Every bug Rust prevents comes from this. Learn it deeply before anything else.

### 📝 Variables, Types & Syntax *(Critical)*
Let bindings, mutability, shadowing, primitive types (integers, floats, bool, char), and basic expressions.

### 🔀 Functions & Control Flow *(Critical)*
Functions, closures, if/else, loop, while, for, and the powerfully expressive `match` statement.

### 🏗️ Structs & Enums *(Critical)*
Custom data types. Enums in Rust are far more powerful than in other languages — they carry data.

---

## Phase 2 — Core Rust Concepts
> What separates real Rust code from toy programs.

### ⚠️ Error Handling — Result & Option *(Core)*
Rust has no exceptions. `Result<T,E>` and `Option<T>` are used everywhere. Learn the `?` operator and common combinators.

### 🧩 Traits *(Core)*
Rust's way of defining shared behavior (like interfaces). Essential for generics and nearly every library you'll use.

### ♾️ Generics *(Core)*
Write functions and types that work across many concrete types without sacrificing performance.

### 📦 Collections — Vec, HashMap, HashSet *(Core)*
The workhorse data structures. Understand their ownership semantics alongside their APIs.

### ⏳ Lifetimes *(Core)*
The hardest concept to grasp. They tell the compiler how long references live. Start with the basics — the compiler's errors are often your best teacher here.

---

## Phase 3 — Practical Rust
> Building real projects.

### 📦 Cargo & the Ecosystem *(Important)*
Rust's build tool and package manager. Learn `Cargo.toml`, crates.io, features, and how to find good crates.

### 🗂️ Modules & Project Structure *(Important)*
How to organise code into modules and crates, control visibility, and avoid spaghetti architecture.

### 🔁 Iterators & Closures *(Important)*
Map, filter, fold, collect — Rust's iterator adapters are zero-cost and extremely expressive. Essential for idiomatic code.

### ✅ Testing *(Important)*
Unit tests (`#[test]`), integration tests, doc tests, and `cargo test`. Testing is a first-class citizen in Rust.

### 🔤 Strings — String vs &str *(Important)*
One of Rust's most confusing early topics. Understand why there are two string types and when to use each.

---

## Phase 4 — Advanced Features
> Unlocking Rust's full power.

### ⚡ Async / Await & Tokio *(Advanced)*
Asynchronous Rust for I/O-heavy workloads. Rust's async model is powerful but has a learning curve. Most web and network code lives here.

### 🧠 Smart Pointers — Box, Rc, Arc, RefCell *(Advanced)*
When ownership rules are too strict, smart pointers give you flexibility. Each trades something different.

### 🧵 Concurrency & Threading *(Advanced)*
Rust prevents data races at compile time. Learn threads, `Mutex`, `Arc`, channels, and why "fearless concurrency" is a real thing.

### 🪄 Macros *(Advanced)*
Declarative macros (`macro_rules!`) and an intro to procedural macros. You'll use macros constantly; building them comes later.

### ⚠️ Unsafe Rust *(Advanced)*
The escape hatch. Sometimes needed for FFI, low-level systems work, or performance-critical code. Understand when and why — and why to use it sparingly.

---

## Phase 5 — Ecosystem & Specialisation
> Pick your domain, go deep.

### 🌐 Web Development — Axum, Actix, Leptos *(Pick one)*
HTTP servers, REST APIs, and full-stack Rust. Axum is the modern go-to; Leptos for WASM-based frontends.

### 💻 CLI Tools — clap, anyhow *(Pick one)*
Rust is excellent for fast, portable command-line tools. Clap for args, anyhow for easy error handling.

### 🕸️ WebAssembly (WASM) *(Pick one)*
Compile Rust to WASM and run it in the browser or edge environments. `wasm-bindgen` and `wasm-pack` are your tools.

### 🔌 Embedded Systems *(Pick one)*
Rust on microcontrollers without an OS. Embassy is the leading async embedded framework. Requires understanding `no_std`.

### 🔬 Advanced Type System *(Optional)*
Trait objects (`dyn Trait`), associated types, HRTBs, newtype pattern, and type-level programming. The deep end.

---

## Tips & Resources

- **Phase 1 is non-negotiable.** Ownership and borrowing is Rust's entire reason for existing. Internalise it before moving on.
- **The Rust Book** — [doc.rust-lang.org/book](https://doc.rust-lang.org/book) — free, well-written, covers phases 1–3 thoroughly.
- **Rustlings** — [github.com/rust-lang/rustlings](https://github.com/rust-lang/rustlings) — hands-on exercises to complement the book.
- **Lifetimes will confuse you — that's normal.** Read the basics, move on, and revisit when the compiler complains.
- **Phase 5 is where you pick a lane.** Most Rust developers focus on systems/CLI, web services, or embedded. You don't need all of it.
