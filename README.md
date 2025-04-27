# `rust-mos-hello-world`

Minimal hello-world example for mos-*-none targets, provided by https://github.com/mrk-its/rust-mos

## Running

The easiest way is to use provided `devcontainer.json` configuration for vscode:

1. Configure Visual Studio Code with `Remote - Containers` extension
2. Open this project inside devcontainer
3. In vscode terminal do:
    ```
      # build for mos-sim-none arch and run in `mos-sim` emulator 
      cargo run 

      # build for mos-atari8-none target
      cargo build --target mos-atari8-none

      # build for mos-nes-nrom-128-none target
      cargo build --target mos-nes-nrom-128-none
    ```

## Additional notes

The toolchain offers only one build target `mos-unknown-none` out of the box.
To build the project for other targets, the docker container contains a python script `/tmp/create_mos_targets.py`.
I have run this script in `build-targets/` and added the results to this repository for convenience.
To build the project for a given target, let's say `mos-nes-nrom`, you can run the following command:
```sh
cargo build --target build-targets/mos-nes-nrom.json
```

## License

All source code (including code snippets) is licensed under either of

- Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or
  [https://www.apache.org/licenses/LICENSE-2.0][L1])

- MIT license ([LICENSE-MIT](LICENSE-MIT) or
  [https://opensource.org/licenses/MIT][L2])

[L1]: https://www.apache.org/licenses/LICENSE-2.0
[L2]: https://opensource.org/licenses/MIT

at your option.
