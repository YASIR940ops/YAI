# YAI YAI (Yet Another Intelligence) Recon Engine

YAI is a high-performance, automated reconnaissance engine written in C and C++. It combines C's low-level non-blocking socket handling with C++'s async multi-threading capabilities to perform fast, scalable port scanning and target assessment.

## Features
- **Low-Level Socket Engine:** C core using non-blocking TCP connections via `select()`.
- **Concurrent Execution:** C++ multi-threading with `std::async` for high throughput scanning.
- **Cross-Platform:** Compatible with Linux, Termux (Android), and macOS.

## Compilation Instructions

To compile **YAI Engine**, run the following command in your terminal:

```bash
g++ -O3 yai_engine.cpp -o yai_engine -lpthread
```

## Usage

Run the compiled executable with default parameters (scans `127.0.0.1` ports `1-1024`):

```bash
./yai_engine
```

Or specify a target IP and port range:

```bash
./yai_engine <TARGET_IP> <START_PORT> <END_PORT>
```

### Example
```bash
./yai_engine 192.168.1.1 20 100
