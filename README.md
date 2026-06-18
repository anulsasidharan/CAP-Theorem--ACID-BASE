# CAP Theorem Explained

An interactive guide to **CAP**, **ACID**, and **BASE** in distributed systems — with real-world examples, architecture diagrams, live simulators, and a decision matrix for system design and interviews.

## Overview

The CAP theorem states that a distributed system can guarantee only **two of three** properties at once:

| Property | Meaning |
|----------|---------|
| **Consistency (C)** | Every read returns the latest write |
| **Availability (A)** | Every request receives a response (no failures) |
| **Partition Tolerance (P)** | The system continues operating despite network splits |

Because network partitions are inevitable in distributed systems, the practical choice is between **CP** (Consistency + Partition Tolerance) and **AP** (Availability + Partition Tolerance).

## What's Included

### Interactive Presentation (`CAP_ACID_BSAE_Explained.html`)

Open this file in any modern browser. No build step or server required.

| Section | Description |
|---------|-------------|
| **CAP Basics** | Core theorem, CP vs AP trade-offs |
| **ACID vs BASE** | Two philosophies for database guarantees |
| **ACID** | Atomicity, Consistency, Isolation, Durability — with rollback diagrams |
| **BASE** | Basically Available, Soft state, Eventual consistency — with replication lag timeline |
| **Isolation Levels** | Read Uncommitted through Serializable |
| **Transaction Simulator** | Side-by-side ACID vs BASE transfer crash demo |
| **CAP Link** | How ACID/BASE map to CP/AP choices |
| **Banking** | CP example — ACID, 2PC, synchronous replication |
| **Amazon Cart** | AP example — eventual consistency, vector clocks |
| **IRCTC** | Hybrid — CP for seat booking, AP for browsing |
| **Partition Simulator** | Live CP vs AP behavior under network partition |
| **Decision Matrix** | CAP choices by system type + database classification |

### Real-World Examples

- **Banking** — Sacrifices availability to prevent double-spending; strict ACID and CP
- **Amazon Shopping Cart** — Prioritizes availability; eventual consistency with conflict resolution
- **IRCTC** — Hybrid model: CP for seat allocation, AP for timetable and search

### Architecture Diagrams

SVG diagrams are embedded throughout the HTML presentation, including:

- CAP pillar model
- ACID rollback flow
- BASE replication lag timeline
- Banking 2PC architecture
- Amazon cart replication
- IRCTC hybrid topology

### CAP Decision Matrix

A reference table mapping common systems and databases to their CAP posture and ACID/BASE characteristics — useful for architecture reviews and interview prep.

## Project Structure

```
.
├── CAP_ACID_BSAE_Explained.html   # Main interactive presentation
├── tasks_requirements.txt         # Task scope and deliverables checklist
├── Cap-ACID-Base.png              # Summary diagram (local)
├── CAP Theorem Final.mp4          # Recorded walkthrough (local)
└── README.md
```

> **Note:** Video and image files are listed in `.gitignore` and are kept locally. Clone the repo and add your own media, or open the HTML file directly — it is fully self-contained.

## Getting Started

1. Clone or download this repository.
2. Open `CAP_ACID_BSAE_Explained.html` in Chrome, Firefox, Edge, or Safari.
3. Use the top navigation to jump between sections.
4. Try the **Transaction Simulator** and **Partition Simulator** for hands-on demos.

## Key Takeaways

- **ACID** implements the **CP** side of CAP — correctness over availability during failures.
- **BASE** implements the **AP** side — availability with eventual consistency.
- There is no universally correct choice; the right trade-off depends on the business domain.
- High-stakes domains (banking, seat booking) lean **CP**; high-traffic consumer apps (carts, feeds) often lean **AP**.

## Requirements Covered

From `tasks_requirements.txt`:

- [x] Consistency, Availability, Partition Tolerance explained
- [x] Banking, Amazon Cart, and IRCTC examples
- [x] Architecture diagrams
- [x] CAP decision matrix
- [x] Practical, interview-ready reference material
