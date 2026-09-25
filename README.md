  # Hossein Amiri

  Systems and backend engineer focused on secure infrastructure, applied cryptography, and network internals. I build low-level tools in Rust, scalable backend services in Python, and
  sandboxed operational platforms.

  ---

  ### What I Work On

  * **Security Infrastructure & Isolation:** Sandboxed runtime environments using hardware-level syscall isolation (gVisor) and loopback-bound operational architectures.
  * **Applied Cryptography:** Ephemeral key derivation, zero-trace file encryption, authenticated headers, and zero-knowledge proof protocols.
  * **Network & Systems Engineering:** Operating system network routing, TUN/TAP virtual adapters, traffic redirection via `iptables`, and packet-level proxying.
  * **Distributed Backend Storage:** Cloud-backed, zero-retention object proxies with streaming chunks and multi-backend failover.
  * **Security Automation & Attack Surface Mapping:** Multi-tier reconnaissance pipelines, automated attack-surface discovery, and headless browser reflection detection engines.

  ---

  ### Featured Projects

  * **[lab-dashboard](https://github.com/HA-ir/lab-dashboard)** — Cybersecurity lab and CTF operations platform with gVisor container orchestration.
    * **What it does:** Orchestrates competitive CTF events, cyber ranges, and automated ephemeral lab lifecycles in front of a headless CTFd engine.
    * **Why it's technically interesting:** Manages disposable container lab lifecycles with hardware-level syscall isolation via gVisor (`runsc`), per-template network egress whitelisting,
  and loopback-isolated middle-tier proxying. Uses Redis Cluster for distributed locking and SSE real-time scoreboards, with automated Playwright E2E verification.
    * **Key technologies:** TypeScript, Next.js, Python, PostgreSQL, Prisma, Redis Cluster, gVisor (`runsc`), Docker, Playwright

  * **[Anbar](https://github.com/HA-ir/Anbar)** — Telegram-backed object storage proxy with zero local file retention.
    * **What it does:** Acts as a two-way streaming upload/download proxy that uses Telegram as an object storage layer while retaining only lightweight SQLite metadata locally.
    * **Why it's technically interesting:** Implements chunked streaming ($\le$16MB) with HTTP range requests, MTProto multi-GB backends, S3 API compatibility, BotPool failover, and
  disaster-recovery channel reconstruction without a local database. Features client-side zero-knowledge encryption (`ANBAR_ZK1` via WebCrypto) and comprehensive automated test suites
  covering adversarial security edge cases (stream stalls, XSS, HMAC validation, cache leaks).
    * **Key technologies:** Python, FastAPI, SQLite (WAL), Docker, WebCrypto, Pyrogram, Pytest

  * **[Cry](https://github.com/HA-ir/Cry)** — Ephemeral, zero-trace command-line cryptography tool.
    * **What it does:** Performs streaming file encryption, deterministic key derivation, and ephemeral SSH credential injection without persisting keys to disk.
    * **Why it's technically interesting:** Implements streaming chunk encryption (AES-256-GCM / ChaCha20-Poly1305) with HMAC-SHA256 authenticated headers, Argon2id key derivation, and
  deterministic Ed25519 identities. Injects derived SSH keys directly into short-lived `ssh-agent` memory with strict zeroization (`zeroize`).
    * **Key technologies:** Rust, Argon2id, AES-GCM, ChaCha20-Poly1305, Ed25519, zeroize, ssh-key

  * **[hotspot-proxy](https://github.com/HA-ir/hotspot-proxy)** — Desktop Wi-Fi hotspot with transparent SOCKS5/HTTP proxy tunneling.
    * **What it does:** Turns a host machine into a Wi-Fi hotspot and transparently routes all connected clients' TCP, UDP, and DNS traffic through an upstream proxy with zero client
  configuration.
    * **Why it's technically interesting:** Integrates `tun2socks` directly into OS-level network layers: `nmcli`, `iproute2`, and `iptables` on Linux; native WinRT tethering and WinTUN
  adapters on Windows. Uses active ARP probing for real-time connected device tracking.
    * **Key technologies:** Rust, Tauri 2, React, TypeScript, iptables, WinTUN, WinRT APIs

  * **[sudoku-zkp](https://github.com/HA-ir/sudoku-zkp)** — Interactive Zero-Knowledge Proof protocol in pure Rust.
    * **What it does:** Allows a prover to prove knowledge of a valid Sudoku solution without revealing any hidden cell values to the verifier.
    * **Why it's technically interesting:** Implements cryptographic commitments (SHA-256) over randomized symbol permutations with interactive verifier challenge-response rounds (rows,
  columns, $3 \times 3$ sub-grids, and given clues), exponentially reducing cheating probability to near zero.
    * **Key technologies:** Rust, SHA-256, Zero-Knowledge Protocols

  ---

  ### Technical Stack

  * **Languages:** Rust, Python, TypeScript, SQL, Bash
  * **Systems & Networking:** Linux Networking (`iptables`, `iproute2`, TUN/TAP interfaces, NetworkManager), Socket Programming, gVisor (`runsc`), Docker
  * **Security & Cryptography:** AEAD (AES-GCM, ChaCha20-Poly1305), Argon2id, Ed25519, Zero-Knowledge Proof Protocols (Commitment schemes, Verifier challenges), WebCrypto, Memory Zeroization
  * **Security Tooling & Automation:** Attack Surface Reconnaissance, Async Headless DOM Analysis (Playwright / Chromium), Network & Subdomain Enumeration
  * **Databases & Storage:** PostgreSQL, SQLite (WAL mode), Redis Cluster (distributed locking, pub/sub), S3 Protocol
  * **Backend Frameworks:** FastAPI, Django, Next.js / Node.js, Tauri 2

  ---

  ### Current Focus

  * Hardening sandboxed orchestration runtimes using container syscall isolation (gVisor).
  * Designing zero-retention, cryptographically partitioned storage backends.
  * Building automated, high-concurrency attack-surface discovery and DOM reflection pipelines.

  ---

  ### Links

  * **Email:** hossein03amiri@gmail.com
  * **LinkedIn:** [hossein-amiri-42aa57439](https://www.linkedin.com/in/hossein-amiri-42aa57439)
  * **Website:** https://amiri-dev.ir
