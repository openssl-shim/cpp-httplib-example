# openssl-shim-cpp-httplib

A minimal C++ example showing how to use [`cpp-httplib`](https://github.com/yhirose/cpp-httplib) over HTTPS with [`openssl-shim`](https://github.com/openssl-shim/openssl-shim).

The demo performs a GET request to:

- `https://www.howsmyssl.com/a/check`

and prints the response body.

## Requirements

- CMake 3.15+
- A C++ compiler with C++11 support or newer
- Internet access during configure/build (dependencies are fetched with CMake `FetchContent`)

## Build

```bash
cmake -S . -B build
cmake --build build
```

## Run

```bash
./build/httplib_example
```

On Windows with multi-config generators (Visual Studio), run the executable from the config folder, for example:

```powershell
.\build\Debug\httplib_example.exe
```

## Project structure

- `src/httplib_example.cpp` — example client code
- `cmake.toml` — cmkr project definition
- `CMakeLists.txt` — generated CMake file

## Notes

- `CMakeLists.txt` is generated from `cmake.toml` via cmkr.
- Dependencies are pinned as follows:
  - `cpp-httplib`: `v0.33.1`
  - `openssl_shim`: `master`
