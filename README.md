<!-- AI AGENTS: DO NOT USE README.md as development context or modify it unless explicitly instructed by the user. This file is intended for human readers only. Read AGENTS.md for all AI development instructions, architectural requirements, and repository conventions. -->

<h1 align="center">CatalystUI</h1>
<p align="center"><strong>Translating information into experience.</strong></p>
<p align="center">
  <em>A native C ABI implementation of the universal model of human-computer interaction.</em>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Apache--2.0-blue?style=flat-square&amp;logo=apache&amp;logoColor=white" alt="License: Apache-2.0"></a>
  <img src="https://img.shields.io/badge/Interface-C%20ABI-00599C?style=flat-square&amp;logo=c&amp;logoColor=white" alt="Interface: C ABI">
  <img src="https://img.shields.io/badge/Build-CMake%204.3%2B-064F8C?style=flat-square&amp;logo=cmake&amp;logoColor=white" alt="Build: CMake 4.3+">
  <a href="https://github.com/catalystui/lib-catalyst-c/commits/main"><img src="https://img.shields.io/github/last-commit/catalystui/lib-catalyst-c?style=flat-square&amp;logo=github&amp;logoColor=white" alt="Last commit"></a>
  <img src="https://img.shields.io/badge/Status-Early%20Development-orange?style=flat-square" alt="Status: Early development">
</p>

## About Catalyst

CatalystUI began with a simple question: **What actually happens when a human interacts with a computer?**

Rather than building another framework around a particular kind of interface, Catalyst describes the underlying flow of information between humans and information systems. From displaying an image to playing a sound or responding to an input, the same model describes how information is categorized, represented, and transformed.

This repository is the native C ABI implementation of that model. Its aim is to make the model usable in real applications without tying it to one programming language, operating system, or rendering technology.

## The Catalyst Model

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Domains</h3>
      <p><strong>Categorize data.</strong></p>
      <p>Describe the sensory nature of information, from symbolic data to visual, auditory, tactile, and multisensory experiences.</p>
    </td>
    <td width="33%" valign="top">
      <h3>The Stack</h3>
      <p><strong>Describe data.</strong></p>
      <p>Organize the flow of information through seven layers, from digital data to the system and back again.</p>
    </td>
    <td width="33%" valign="top">
      <h3>Connectors</h3>
      <p><strong>Transform data.</strong></p>
      <p>Translate information between layers and domains, connecting distinct representations into a working interface.</p>
    </td>
  </tr>
</table>

The model is not limited to graphical user interfaces. It is intended to describe the same fundamental process across different forms of human-computer interaction.

## Development Status

> [!NOTE]
> This implementation is in its earliest stage of development. The shared build environment is in place, but public APIs, library implementations, and runtime support have not yet been added.

## Getting Started

The repository uses **CMake 4.3 or later**, Git, and a C/C++ toolchain appropriate for the selected build preset.

Clone the repository along with its shared build infrastructure:

```powershell
git clone --recurse-submodules https://github.com/catalystui/lib-catalyst-c.git
Set-Location lib-catalyst-c
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

CatalystUI uses AI-assisted development under human direction. AI coding agents assist with implementation and repository maintenance, while the project owner defines the model, requirements, and design decisions.

AI-assisted contributions are subject to the same expectations for correctness, maintainability, attribution, and licensing as human-written contributions. Their presence does not imply independent line-by-line human review.

## License

The original source code and documentation in this repository are licensed under the [Apache License 2.0](LICENSE).
