## About

This template is designed for writing [Zellij][zellij] plugins in Rust.

You can learn more about developing plugins in the [Zellij Documentation][docs].

[zellij]: https://github.com/zellij-org/zellij
[docs]: https://zellij.dev/documentation/plugins.html

## Usage

### Use `cargo generate` to Clone this Template

[Learn more about `cargo generate` here.](https://github.com/ashleygwilliams/cargo-generate)

```
cargo generate --git https://github.com/zellij-org/rust-plugin-template.git --name my-project
cd my-project
```

### Build with `cargo` and Test in Zellij

```sh
# If you don't have Zellij installed already
cargo install zellij
# Building the plugin
cargo build
# Running in Zellij
zellij -l plugin.yaml
```
## Current Plan
The basic idea for this plugin is to have a neutral position inside Zellij. I'm
not interested in immense detail, but rather something like the dashboard in 
doom emacs. Some features would be:
- Date & Time
- Calendar Integration? (idk how to get this working, but i'd like it to work with macOS)
- Zellij Tab View (+ keybindings)
- Simple keybindings:
  - T for terminal (or terminal tab)
  - J for julia repl (or julia repl tab)
  - E for editor (or editor tab)
  - S for script dir?
  - U for updates (brew, rustup, npm, julia, etc.)
  - and more, that should probably be customizable. These are just good defaults.
- Results of previous commands (U/T/J)
- Theming sync with Zellij