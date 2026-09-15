

![PEDIT COW](pedit.png)

CVE-2026-46331 is a Linux kernel privilege escalation vulnerability involving the traffic control subsystem and page cache corruption.


Requirements:
Linux x86_64
GCC
iproute2
tc
Vulnerable kernel

Exploitation Flow:

SUID Enumeration
        ↓
Target Selection
        ↓
ELF Analysis
        ↓
tc / Netlink / pedit
        ↓
Page Cache Corruption
        ↓
Corruption Verification
        ↓
SUID Execution
        ↓
Privilege Escalation
