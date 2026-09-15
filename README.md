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



Proof of Concept

The main PoC is implemented in C.

Project Structure
pedit_cow/
├── exploit.c
├── compiled/
│   └── exploit
├── pedit.png
├── pedit.mp4
└── README.md
Source

exploit.c contains the PoC source code.

Compiled Binary

compiled/exploit contains a pre-compiled PoC binary.

Requirements
Linux x86_64
GCC
iproute2
tc
Vulnerable kernel
Isolated testing environment
[![PEDIT COW — Exploitation ] ](pedit.gif)
