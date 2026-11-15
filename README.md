<!-- AI AGENTS: DO NOT USE README.md as development context or modify it unless explicitly instructed by the user. This file is intended for human readers only. Read AGENTS.md for all AI development instructions, architectural requirements, and repository conventions. -->

<h1 align="center">Crystal</h1>
<p align="center"><strong>The universal translator between computers and people.</strong></p>
<p align="center">
  <em>The native windowing ABI for CatalystUI.</em>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-blue?style=flat-square&amp;logo=apache&amp;logoColor=white" alt="License: Apache-2.0"></a>
  <img src="https://img.shields.io/badge/Interface-C%20ABI-00599C?style=flat-square&amp;logo=c&amp;logoColor=white" alt="Interface: C ABI">
  <img src="https://img.shields.io/badge/CatalystUI-Window%20Layer-526b80?style=flat-square" alt="CatalystUI: Window layer">
  <img src="https://img.shields.io/badge/Build-CMake%204.3%2B-064F8C?style=flat-square&amp;logo=cmake&amp;logoColor=white" alt="Build: CMake 4.3+">
  <a href="https://github.com/catalystui/lib-crystal-c/commits/main"><img src="https://img.shields.io/github/last-commit/catalystui/lib-crystal-c?style=flat-square&amp;logo=github&amp;logoColor=white" alt="Last commit"></a>
  <img src="https://img.shields.io/badge/Status-Early%20Development-orange?style=flat-square" alt="Status: Early development">
</p>

## About Crystal

Crystal is the windowing library for CatalystUI, implementing **Layer 2: Window** of the CatalystUI model through a native C ABI.

A window provides a view into the underlying system through which an application can receive interactions and deliver output. Crystal aims to provide a consistent, portable interface for working with these windows across platforms, without tying applications to a particular programming language or rendering technology.

Crystal is focused on windowing, not rendering or higher-level UI components. Its purpose is to provide the connection point through which those systems can interact with the underlying platform.

## Development Status

> [!NOTE]
> This implementation is in its earliest stage of development. The shared build environment is in place, but public APIs, library implementations, and runtime support have not yet been added.

## Getting Started

The repository uses **CMake 4.3 or later**, Git, and a C/C++ toolchain appropriate for the selected build preset.

Clone the repository along with its shared build infrastructure:

```powershell
git clone --recurse-submodules https://github.com/catalystui/lib-crystal-c.git
Set-Location lib-crystal-c
cmake --list-presets
```

If the repository has already been cloned, initialize its submodule with:

```powershell
git submodule update --init --recursive
```

The shared presets define target-specific compiler and platform configurations. For example, on an Apple Silicon Mac with the required Xcode toolchain:

```powershell
cmake --preset aclang17-darwin24.6-arm64
```

There are currently no library targets to compile. Preset availability depends on the host and installed toolchain; the presence of a preset does not imply verified runtime support.

## Related Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/catalystui/lib-core-c">lib-core-c</a></h3>
      <p>Foundational C ABI libraries for CatalystUI core types, memory management, and text encoding.</p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/catalystui/build-cmake">build-cmake</a></h3>
      <p>Shared CMake configuration, target metadata, and platform-specific build presets for CatalystUI's native libraries.</p>
    </td>
  </tr>
</table>

## AI-Assisted Development

Crystal is developed with AI assistance under human direction. AI coding agents assist with implementation and repository maintenance, while the project owner defines the model, requirements, and design decisions.

AI-assisted contributions are subject to the same expectations for correctness, maintainability, attribution, and licensing as human-written contributions. Their presence does not imply independent line-by-line human review.

## License

The original source code and documentation in this repository are licensed under the [Apache License 2.0](LICENSE).
