[English](./README.md) | [中文](./README.zh-CN.md)

# CS168 Study Repository

A personal study repository for **Berkeley CS168 — Introduction to the Internet: Architecture and Protocols** (Spring 2025), using Claude Code as an AI tutor with a Socratic teaching methodology.

**GitHub**: [github.com/elecMa517](https://github.com/elecMa517)

---

## What This Repository Does

Claude Code acts as an interactive CS168 tutor that:

- Asks what you already know before explaining anything (no direct answers)
- Checks your understanding with follow-up questions after each explanation
- Automatically documents every session — what you learned, what you mastered, what gaps remain
- Works through disc worksheets in `reference/` alongside you

---

## Repository Structure

```
/reference/                       # Place disc PDFs here locally (git-ignored, see links below)

/sessions/                        # Daily learning session notes
  /YYYY-MM-DD/
    session-notes.md
  SESSION-TEMPLATE.md

/progress/
  cs168-study-tracker.md          # Single source of truth: all 48 topics tracked

CLAUDE.md                         # AI tutor instructions
README.md                         # This file (English)
README.zh-CN.md                   # Chinese version
```

---

## Discussion Worksheets (Official Links)

All PDFs are hosted on the official CS168 SP25 course website. Download them into your local `reference/` folder.

| Disc | Topic | Worksheet | Solutions |
|------|-------|-----------|-----------|
| 01 | Network Architecture, Layers, Traceroute | [disc01](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc01.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc01-sols.pdf) |
| 02 | Packet Switching, Delays, Statistical Multiplexing | [disc02](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc02.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc02-sols.pdf) |
| 03 | Distance-Vector Routing (Bellman-Ford) | [disc03](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc03.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc03-sols.pdf) |
| 04 | Link-State Routing (Dijkstra / OSPF) | [disc04](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc04.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc04-sols.pdf) |
| 05 | BGP — Interdomain Routing | [disc05](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc05.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc05-sols.pdf) |
| 06 | TCP — Reliable Transport | [disc06](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc06.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc06-sols.pdf) |
| 07 | Congestion Control (AIMD, Slow Start) | [disc07](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc07.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc07-sols.pdf) |
| 08 | DNS, HTTP, Ethernet | [disc08](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc08.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc08-sols.pdf) |
| 09 | ARP, DHCP, NAT | [disc09](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc09.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc09-sols.pdf) |
| 10 | Datacenters & SDN | [disc10](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc10.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc10-sols.pdf) |
| 11 | Host Networking (Kernel Stack, RDMA) | [disc11](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc11.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc11-sols.pdf) |
| 12 | Multicast & Collective Communication | [disc12](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc12.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc12-sols.pdf) |

---

## How to Use

### Step 1: Setup

```bash
git clone https://github.com/elecMa517/Network-Study.git
cd Network-Study
```

Install [Claude Code](https://claude.ai/code), then run it inside the repo:

```bash
claude
```

### Step 2: Start Learning

Just ask questions naturally — like talking to a tutor:

```
"I want to learn distance-vector routing from disc03"
"How does TCP's sliding window work?"
"Help me work through disc06 question 1"
```

Claude will ask about your existing understanding first, then explain, then ask a follow-up question to verify you actually got it.

### Step 3: Work Through Disc Problems

```
"Let's work through disc04 together"
"I'm stuck on the BGP problem in disc05"
```

Claude reads the PDF from `reference/` and guides you with hints — not immediate answers.

### Step 4: Review Weak Areas

```
"What topics do I still not understand?"
"Review my weakest points from recent sessions"
```

Claude reads `progress/cs168-study-tracker.md` and recent session notes to give you targeted review.

### After Each Session

No manual action needed — Claude automatically:
1. Creates `sessions/YYYY-MM-DD/session-notes.md` with what was covered and where you struggled
2. Updates `progress/cs168-study-tracker.md` with new progress and knowledge gaps

---

## Recommended Study Order

`disc01 → disc02 → disc03+04 → disc05 → disc06+07 → disc08+09 → disc10 → disc11+12`

Start with disc01 to build the layering mental model — everything else depends on it.

---

## Authoritative Sources

- **Kurose & Ross** *Computer Networking: A Top-Down Approach*
- **Tanenbaum & Wetherall** *Computer Networks*
- **RFCs**: RFC 793 (TCP), RFC 791 (IP), RFC 4271 (BGP), etc.
- Disc PDFs from [sp25.cs168.io](https://sp25.cs168.io/) (primary course practice materials)

---

## Acknowledgements

- **CS168 — UC Berkeley**: All discussion worksheets and course materials are from the [CS168 Spring 2025](https://sp25.cs168.io/) course. This repository is an independent study tool and is not affiliated with or endorsed by UC Berkeley or the CS168 course staff.

- **[chenran818/CFP-Study](https://github.com/chenran818/CFP-Study)**: The repository structure, session tracking protocol, and Socratic teaching methodology in `CLAUDE.md` are adapted from this project, which used the same AI-powered guided learning approach to prepare for the CFP exam.
