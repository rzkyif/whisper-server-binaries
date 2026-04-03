# whisper.cpp server binaries

Pre-compiled [whisper-server](https://github.com/ggml-org/whisper.cpp) binaries for macOS, Linux, and Windows.

## Supported Platforms

| Platform | Architecture | GPU Acceleration | Notes |
|----------|-------------|------------------|-------|
| macOS    | Apple Silicon (arm64) | ✅ Metal | Native build |
| macOS    | Intel (x86_64)       | ✅ Metal | Native build |
| Linux    | x86_64               | ❌ CPU-only | Native build |
| Linux    | x86_64               | ✅ Vulkan | Requires Vulkan-capable GPU drivers |
| Linux    | ARM64                | ❌ CPU-only | Cross-compiled via aarch64-linux-gnu |
| Windows  | x64                  | ❌ CPU-only | LLVM/Clang build |
| Windows  | x64                  | ✅ Vulkan | Requires Vulkan-capable GPU drivers |
| Windows  | ARM64                | ❌ CPU-only | Cross-compiled via LLVM/Clang |

## Release Artifacts

Each release contains a zip per platform:

```
whisper-server-{version}-{platform}-{arch}[-vulkan].zip
├── whisper-server[.exe]
└── ... necessary libraries ...
```

## Automatic Updates

This repository automatically checks [ggml-org/whisper.cpp](https://github.com/ggml-org/whisper.cpp) for new releases daily at **00:00 UTC**. When a new version is detected, a build is triggered automatically and a release is published with all binaries.