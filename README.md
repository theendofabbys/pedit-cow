# PEDIT COW

![PEDIT COW](pedit.png)

> **Proof of Concept — Linux Kernel Privilege Escalation**

---

## CVE-2026-46331

**CVE-2026-46331** is a Linux kernel privilege escalation vulnerability involving the traffic control subsystem, Netlink, `pedit`, and page cache corruption.

This repository contains a Proof of Concept demonstrating the exploitation flow in a controlled environment.

---

## Overview

The vulnerability involves an interaction between Linux traffic control mechanisms and kernel memory/page-cache handling.

The PoC demonstrates the following general exploitation chain:

```text
SUID Enumeration
       │
       ▼
Target Selection
       │
       ▼
ELF Entry Point Detection
       │
       ▼
tc / Netlink / pedit
       │
       ▼
Page Cache Corruption
       │
       ▼
Corruption Verification
       │
       ▼
SUID Binary Execution
       │
       ▼
Elevated Privileges
