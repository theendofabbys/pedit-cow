
Proof of Concept for a Linux kernel privilege escalation vulnerability involving `tc`, netlink `pedit`, and page cache corruption.


## Project Structure

pedit_cow/
├── exploit.c
├── compiled/
│   └── exploit
└── README.md

* `exploit.c` — PoC source code.
* `compiled/exploit` — Pre-compiled PoC binary.
* `README.md` — Project documentation.

## Compilation

To compile the PoC yourself:

gcc -Wall -Wextra exploit.c -o exploit

You can then place the resulting binary inside `compiled/`:

mkdir -p compiled
mv exploit compiled/

## Usage

Using the pre-compiled binary:

./compiled

Or compile and run your own build:

```bash
gcc -Wall -Wextra exploit.c -o exploit
./exploit
```

## Execution Flow

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

## Requirements

* Linux x86_64
* Vulnerable kernel
* GCC
* `iproute2`
* `tc`

