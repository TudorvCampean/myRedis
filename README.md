# myRedis

A lightweight, from-scratch implementation of a Redis-like in-memory data store written in C++.

## What is Redis?

**Redis** (REmote DIctionary Server) is an open-source, in-memory data structure store used as a database, cache, message broker, and streaming engine. Key characteristics include:
- **In-Memory Storage:** Data resides in RAM for sub-millisecond response times and high throughput.
- **Key-Value & Rich Data Structures:** Supports strings, hashes, lists, sets, sorted sets, bitmaps, and streams.
- **Event-Driven Architecture:** Uses non-blocking I/O and an event loop to handle thousands of concurrent client connections efficiently without the overhead of thread-per-connection concurrency.

---

## Project Status (Work in Progress)

This repository contains an educational, ground-up implementation exploring network programming and event-driven architectures behind Redis:

- **Non-blocking I/O Event Loop:** Implemented using `poll()` to multiplex multiple TCP connections.
- **Length-Prefixed Framing Protocol:** Client and server communicate using a custom length-prefixed protocol over TCP sockets.
- **Core Components:**
  - `tcp_server.cpp`: Event-driven TCP server handling concurrent connections, buffer management, and request processing.
  - `tcp_client.cpp`: TCP client sending pipelined/length-prefixed requests and receiving responses.

---

## Building and Running

### Prerequisites
- C++17 compiler (GCC or Clang)
- CMake 3.10+
- Linux environment

### Build
```bash
mkdir -p build
cd build
cmake ..
cmake --build .
```

### Run
1. Start the server:
   ```bash
   ./build/server
   ```

2. In another terminal, run the client:
   ```bash
   ./build/client
   ```
