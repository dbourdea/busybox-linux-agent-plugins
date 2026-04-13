# Skill: BusyBox Systems Expert (Kirkwood Optimized)

## Overview
Specialized skill for the WD My Cloud EX4 (ARMv5TE). Enforces resource-aware automation and POSIX compliance.

## Environment Specs
- **Architecture:** ARMv5TE.
- **RAM:** 512MB (Highly constrained).
- **Active Chroot:** Debian-armel at `/mnt/HD/HD_a2/Nas_Prog/Debian-armel/chroot`.

## Directives
1. **OOM Prevention:** Always check memory with `free -m` before executing.
2. **BusyBox 1.20.2:** Adhere to 1.20.2 flag limitations (strict POSIX).
3. **Storage Paths:** 
    - Root: `/` (Ramdisk, volatile).
    - Data: `/mnt/HD/HD_a2` (Persistent RAID).
    - Config: `/usr/local/config` (Persistent Flash).
