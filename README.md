# Dr. Mario 64 Capsule+ Mod
**Capsule+ is under active development in the capsuleplus branch. Until it's ready to merge into master, this branch is a matching decomp.**

## Mod Overview

The goal of this mod is to create an **expanded capsule preview system**:
- While the original game only shows the next capsule coming up, the mod aims to display the **next 3–4 capsules**.
- This will hopefully encourage **deeper strategy**, especially to **assist in attack moves** in multiplayer modes.

### Based On

This project builds on the [matching decomp of Dr. Mario 64](https://github.com/AngheloAlf/drmario64) by AngheloAlf. Please refer to their repository for additional information.

## Quick Setup

### System Dependencies
Install the following packages (Ubuntu / WSL2 recommended):

```
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

If successful, the final ROM will be located at:
```
./build/us/drmario64.us.z64
```
