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
/reference/                       # CS168 SP25 discussion worksheets (+ solutions)
  cs168-sp25-disc01.pdf           # Layers, Design, Traceroute
  cs168-sp25-disc01-sols.pdf      # Solutions
  ... disc02 through disc12 ...

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

## Topics Covered (disc01–12)

| Disc | Topic |
|------|-------|
| 01 | Network Architecture, Layers, Traceroute |
| 02 | Packet Switching, Delays, Statistical Multiplexing |
| 03 | Distance-Vector Routing (Bellman-Ford) |
| 04 | Link-State Routing (Dijkstra / OSPF) |
| 05 | BGP — Interdomain Routing |
| 06 | TCP — Reliable Transport |
| 07 | Congestion Control (AIMD, Slow Start) |
| 08 | DNS, HTTP, Ethernet |
| 09 | ARP, DHCP, NAT |
| 10 | Datacenters & SDN |
| 11 | Host Networking (Kernel Stack, RDMA) |
| 12 | Multicast & Collective Communication |

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
- Disc PDFs in `reference/` (primary course practice materials)
