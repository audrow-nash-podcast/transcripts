# README

## Local Development

To run locally, make sure you have [Rust](https://www.rust-lang.org/tools/install) and [mdBook](https://rust-lang.github.io/mdBook/guide/installation.html) installed.

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
cargo install mdbook
```

After mdbook is installed, you can start a local development server with the following command:

```bash
mdbook serve
```

If port 3000 is taken, you can use a different port with `-p <port>`.
