# An I/O Project: Building a Command Line Program (Rust Book Chapter 12)

This is my implementation of the **Chapter 12 project ("An I/O Project: Building a Command Line Program")** from *The Rust Programming Language*.
It’s a small clone of `grep`, written in Rust, that searches for a string in a file.

## Features

* Accepts a **query string** and a **file path** via command-line arguments
* Reads file contents and returns lines containing the query
* Supports **case-insensitive search** via the `IGNORE_CASE` environment variable
* Prints results to **stdout**, and error messages to **stderr**
* Built incrementally with **test-driven development (TDD)**

## Usage

```bash
# Basic case-sensitive search
cargo run -- searchstring poem.txt

# Case-insensitive search using environment variable
IGNORE_CASE=1 cargo run -- searchstring poem.txt
```

Example:

```bash
$ cargo run -- frog poem.txt
How public, like a frog
```

Redirect output to a file:

```bash
cargo run -- to poem.txt > output.txt
```

Errors are written to **stderr**, so they still appear on the terminal.

## Tests

Run the test suite with:

```bash
cargo test
```

## License

This project is licensed under the [MIT License](LICENSE).
The Rust Book and example code are also available under MIT OR Apache-2.0.
