## Tauri.js

**Cannot compile Tauri app's `msi` in WSL. Must do so in Powershell (admin)**

## Windows

Visit the Tauri official docs and follow installing and setting up the prerequitsites for Tauri to run and compile.

- https://tauri.app/v1/guides/getting-started/prerequisites

  1. Set up **Microsoft Visual Studio C++ Build Tools** (https://visualstudio.microsoft.com/visual-cpp-build-tools/)
     - Tick **Desktop development with C++**
     - Tick `MSVC v143 - VS 2022 C++ x64/x86 build...` and `Windows 10 SDK` under _Optional_
  2. If you're on Windows 10, install WebView2 Runtime (https://developer.microsoft.com/en-us/microsoft-edge/webview2/#download-section)
  3. Now install Rust. Go to https://www.rust-lang.org/tools/install or run `winget install --id Rustlang.Rustup` in Powershell.

- Open the directory in Powershell (admin)

- Rename `identifier` to be something else unique - To make compilation faster, remember change `targets` to something like `["msi"]`

- To compile and make the msi and whatever use, you must use the Tauri CLI. So, `yarn tauri build`.

## Ubuntu

```
sudo apt install pkg-config \
  libdbus-1-dev \
  libgtk-3-dev \
  libsoup2.4-dev \
  libjavascriptcoregtk-4.0-dev \
  libwebkit2gtk-4.0-dev
```

## References:

https://visualstudio.microsoft.com/visual-cpp-build-tools

https://tauri.app/v1/guides/getting-started/prerequisites

https://www.rust-lang.org/tools/install
