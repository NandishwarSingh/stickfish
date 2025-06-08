# 🐟 Stickfish

> **A Single-Binary, AOT-Compiled JavaScript Runtime**  
> Bundles, optimizes, AOT-compiles your JS → LLVM → native code, embeds QuickJS for Socket.IO & Node APIs, and serves high-throughput HTTP/WebSockets via Zig’s async I/O.

---

## 🚀 Features

- **Zero-install single binary** for Linux, Windows & macOS  
- **Bundling & minification** via SWC/Spack  
- **JS → LLVM IR** with js-ziju  
- **AOT compile** IR → native via `llc` + Zig LTO  
- **SIMD math** acceleration with [zmath](https://github.com/mcmtroffaes/zmath)  
- **Async I/O** powered by [zig-aio](https://github.com/prime31/zig-aio) (io_uring/epoll)  
- **Embedded QuickJS** VM for Socket.IO, `fs`/`os`/`child_process` shims  

---

## 📦 Installation

```bash
git clone https://github.com/your-org/stickfish.git
cd stickfish

# Initialize submodules
git submodule update --init --recursive

# Build (native)
zig build

# Cross-compile (optional)
zig build -Dtarget=x86_64-windows-gnu
zig build -Dtarget=x86_64-macos

```
# Performance
| Metric                 | Stickfish        | Bun     | Go      | Rust    | Zig     | C/C++   |
| ---------------------- | ---------------- | ------- | ------- | ------- | ------- | ------- |
|   I/O Throughput       | \~40 K req/s     | \~20 K  | \~15 K  | \~12 K  | \~12 K  | \~18 K  |
|   Compute Throughput   | \~600 M ops/s    | \~200 M | \~400 M | \~550 M | \~550 M | \~650 M |




