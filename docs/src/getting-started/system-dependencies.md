# System Requirements

There are several system requirements including fuelup, llvm, clang and postgres.

## Fuel system dependencies

Getting started with a Fuel indexer requires a single primary dependency from the Fuel ecosystem -- `fuelup`
- `fuelup` installs the Fuel toolchain from Fuel's official release channels, enabling you to easily keep the toolchain updated. For more info, take a look at the [`fuelup` repo](https://github.com/fuellabs/fuelup).

### Installation

To install `fuelup`

```bash
fuelup toolchain install latest
```

## Other system dependencies

### Ubuntu/Debian

```bash
apt update
apt install -y cmake pkg-config git \
    gcc build-essential clang libclang-dev llvm libpq-dev
```

| Dependency | Required For |
| --------------- | --------------- |
| cmake | Manages the build process in an operating system and in a compiler-independent manner |
| pkg-config | Language-agnostic helper tool used when compiling applications and libraries |
| git | Version control system |
| gcc | Compiler tools required to build various Fuel Indexer crates |
| clang | Compiler tools required to build various Fuel Indexer crates on Unix-like OSes |
| llvm | Required for building Fuel Indexer crate dependencies |
| libpq-dev | Set of library function helping facilitate interaction with the PostgreSQL backend |

### MacOS

```bash
brew update
brew install cmake llvm libpq postgresql
```

| Dependency | Required For |
| --------------- | --------------- |
| cmake | Manages the build process in an operating system and in a compiler-independent manner |
| llvm| Compiler infrastructure for building Fuel Indexer crate dependencies |
| libq | Postgres C API library |
| postgresql | Installs the command line console (psql) as well as a PostgreSQL server locally  |

### Arch

```bash
pacman -Syu --needed --noconfirm cmake \
    gcc pkgconf git clang llvm11 llvm11-libs postgresql-libs
```

| Dependency | Required For |
| --------------- | --------------- |
| cmake | Manages the build process in an operating system and in a compiler-independent manner |
| git | Version control system |
| gcc | Compiler tools required to build various Fuel Indexer crates |
| llvm11 | Compiler infrastructure for building Fuel Indexer crate dependencies |
| llvm11-libs | Compiler infrastructure libs for building Fuel Indexer crate dependencies |
| pkgconf | System for configuring build dependency information |
| postgresql-libs | Provides the essential shared libraries for any PostgreSQL client program or interface |
| clang | Compiler required to build various Fuel Indexer crates Unix-like OSes |
