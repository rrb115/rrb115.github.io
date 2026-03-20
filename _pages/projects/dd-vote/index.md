---
title: "Distributed Democracy Vote"
permalink: /projects/dd-vote/
layout: home
author_profile: false
---

<p><b>Distributed Democracy Vote</b> is a simulated voting system that demonstrates fault tolerance and leader coordination across multiple Java-based servers while a client application lets users register, log in, and vote.</p>

<p>Servers communicate over sockets, elect leaders via the Bully algorithm, and exchange heartbeats so the cluster can detect failures and recover without losing in-flight votes.</p>

### Tech Stack

- Java
- Networking (Sockets)
- Distributed Systems Concepts

### Highlights

- Designed and implemented a fault-tolerant distributed voting system simulation.
- Utilized a client-server architecture and implemented the Bully algorithm for leader election.
- Incorporated heartbeat mechanisms for server liveness detection and failure handling.
