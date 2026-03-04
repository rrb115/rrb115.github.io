---
title: "Verifiable Distributed Configuration System (VDCS)"
permalink: /projects/vdcs/
layout: minimal-home
author_profile: false
---

<p><b>VDCS</b> is a cryptographically verifiable, append-only configuration store that lets consumers prove the integrity of every value they read.</p>

<p>Applications can consume configuration (like feature flags or database hosts) without blindly trusting the control plane because every change is signed, logged, and accompanied by a Merkle proof.</p>

### Tech Stack

- Ed25519 signatures
- SHA-256 Merkle trees and proofs
- gRPC server with Protobuf-based protocol

### Key Features

- Trustless: clients verify Merkle proofs for every value they consume.
- Immutable: every change is signed and appended to a hash-linked cryptographic log.
- Auditable: the entire history is tamper-evident and can be inspected by third parties.
- Fast: leverages Ed25519 and SHA-256 primitives for compact proofs and signatures.

### Architecture

- Node: a gRPC server responsible for managing the Log and State.
- Client: a CLI (and future SDK) that proposes signed changes and verifies proofs.
- Protocol: a custom Protobuf-based protocol that enforces strict verification at every step.
