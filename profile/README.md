# Tyrionic

Tyrionic is a small compiled programming language with a self-hosting compiler.
Tyrionic programs compile to standalone native executables, while a compact C
seed provides a reproducible path for bootstrapping the compiler from source.

## Projects

- [tyrionic/tyrionic](https://github.com/tyrionic/tyrionic) contains the
  Tyrionic compiler, written in Tyrionic, together with examples and extension
  sources.
- [tyrionic/tyrionc](https://github.com/tyrionic/tyrionc) contains the C
  bootstrap compiler used to build the first Tyrionic compiler generation.
- [tyrionic/tyrionic-tests](https://github.com/tyrionic/tyrionic-tests)
  contains the independent bootstrap, fixed-point, diagnostic, and application
  acceptance suite.

## Install with Homebrew

```sh
brew tap tyrionic/tyrion
brew trust tyrionic/tyrion
brew install tyrion
```

Confirm the installation:

```sh
tyrionic --version
```

## Compile a Program

```sh
cat > hello.ty <<'TYRIONIC'
print("Hello from Tyrionic")
TYRIONIC

tyrionic --build hello.ty --out hello
./hello
```

Tyrionic is available under the MIT License.
