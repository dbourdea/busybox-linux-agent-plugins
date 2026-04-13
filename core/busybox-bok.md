# Skill: BusyBox & Embedded Systems Expert (Kirkwood Optimized)

## Overview
Optimized for the Marvell Kirkwood (ARMv5TE) architecture and WD My Cloud EX4 environments. This skill enforces resource-aware automation and POSIX-strictness.

## Discovery Context (WD My Cloud EX4)
- **CPU:** ARMv5TE @ 2.0 GHz (Feroceon 88FR131).
- **RAM:** 512MB (Critical Constraint).
- **Environment:** BusyBox v1.20.2.
- **Modernization:** Pivot to Debian chroot at `/mnt/HD/HD_a2/Nas_Prog/Debian-armel/chroot` for modern library support.

## Technical Mandates

### 1. Memory Safety
- **Restriction:** Never launch heavy processes on the native system.
- **Guideline:** Favor small `awk` and `sh` scripts for native data processing.

### 2. POSIX-Strict Scripting
- **Interpreter:** Always use `#!/bin/sh`.
- **Syntax:** 
    - No arrays.
    - No `[[ ]]`. Use `[ ]` with variable quoting.
    - Use `printf` for all formatted output.

### 3. Tool-Specific Standards (BusyBox 1.20.2)
- **sed:** Mandatory backup suffix for in-place edits (`sed -i.bak`).
- **grep:** BRE/ERE only. No Perl Regex.
- **find:** No `-printf`. Use `ls -l | awk`.

### 4. Hardware Persistence
- **Storage:** Data resides in `/mnt/HD/HD_a2`.
- **Boot:** System settings are in `/usr/local/config/config.xml`.
- **Swap:** Utilize the identified 6.2GB swap partition for analytical tasks.
