# BusyBox: The Multi-Call Binary Architecture

BusyBox is a single multi-call binary designed for resource-constrained systems. It dispatches applets based on `argv[0]`.

## 🧠 Critical Technical Knowledge
- **The Multi-Call Dispatcher:** Every BusyBox tool is a symlink to `/bin/busybox`. Direct execution via `/bin/busybox [applet]` is the safest method if symlinks are unreliable.
- **Applet Discovery:** Use `busybox --list` to verify exactly which tools are compiled into the binary.
- **The ash Shell (POSIX):** Assume Almquist Shell. No bashisms allowed.
- **Regex Limitations:** No PCRE (`grep -P`). Only BRE/ERE.
- **In-place Editing:** `sed -i` requires a backup suffix (e.g., `sed -i.bak`).

## 🛠️ Modernization Path
1. **Probe:** `cat /proc/cpuinfo` for architecture.
2. **Unlock:** Static binaries from `busybox.net`.
3. **Expand:** Bootstrap `Entware` to `/opt`.
