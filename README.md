# Dr. Mario 64

[![Build Status]][actions] ![Code us Progress] ![Code cn Progress] ![Code gw Progress]

[Build Status]: <https://github.com/AngheloAlf/drmario64/actions/workflows/ci.yml/badge.svg>
[actions]: <https://github.com/AngheloAlf/drmario64/actions/workflows/ci.yml>
[Code us Progress]: https://img.shields.io/endpoint?label=Code%20us&url=https%3A%2F%2Fprogress.deco.mp%2Fdata%2Fdrmario64%2Fus%2Fcode%2F%3Fmode%3Dshield%26measure%3Dall
[Code cn Progress]: https://img.shields.io/endpoint?label=Code%20cn&url=https%3A%2F%2Fprogress.deco.mp%2Fdata%2Fdrmario64%2Fcn%2Fcode%2F%3Fmode%3Dshield%26measure%3Dall
[Code gw Progress]: https://img.shields.io/endpoint?label=Code%20gw&url=https%3A%2F%2Fprogress.deco.mp%2Fdata%2Fdrmario64%2Fgw%2Fcode%2F%3Fmode%3Dshield%26measure%3Dall

Matching decomp of Dr. Mario 64

[Progress graph :chart_with_upwards_trend:](https://angheloalf.github.io/drmario64/)

## Dependencies

All the instructions assume the user is using a Debian/Ubuntu based Linux
distro. If you are a Windows user then it is recommended to use WSL2 with
Ubuntu.

### System packages

The build process has the following package requirements:

* make
* git
* build-essential
* clang
* binutils-mips-linux-gnu
* gcc-mips-linux-gnu
* python3
* pip3
* venv
* Rust

Under Debian / Ubuntu (which we recommend using), you can install them with the following commands:

```bash
sudo apt update
sudo apt install make git build-essential clang binutils-mips-linux-gnu gcc-mips-linux-gnu python3 python3-pip python3-venv
```

### Python Environment
```
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -U -r requirements.txt
```

### Rust and Extra Tools
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
cargo install pigment64 --version ">=0.3.0,<1.*"
```

## Build (Condensed)
Copy your big-endian Dr Mario 64 ROM (renamed as `baserom.us.z64`) into the repository's `./config/us/` directory. Then run:

```
make setup
make lib
make extract
make
```

If successful, the modded ROM will be located at:
```
./build/us/drmario64.us.z64
```
