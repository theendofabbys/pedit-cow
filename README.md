CVE-2026-46331 is a Linux kernel privilege escalation vulnerability involving the traffic control subsystem, Netlink, pedit, and page cache corruption.

This repository contains a Proof of Concept demonstrating the exploitation flow in a controlled environment.

Overview

The vulnerability involves an interaction between Linux traffic control mechanisms and kernel memory/page-cache handling.

The PoC demonstrates the following general exploitation chain:

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
Proof of Concept

The main PoC is implemented in C:

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

Exploitation Demonstration

Click the image below to open the exploitation video:




Mitigation

The recommended mitigation is to update the Linux kernel to a version containing the appropriate security fix.

Check the currently running kernel:

uname -r

On Debian-based systems:

sudo apt update
sudo apt upgrade

Administrators should verify the affected and fixed kernel versions against the security advisory for their specific Linux distribution.

Requirements
Linux x86_64
GCC
iproute2
tc
Vulnerable kernel
Isolated testing environment
