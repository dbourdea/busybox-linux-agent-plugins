# BusyBox Linux Agent Plugins

A professional-grade repository for managing, modernizing, and automating minimal Linux environments powered by BusyBox. Specifically optimized for ARMv5 (Marvell Kirkwood) and legacy embedded systems.

## 📁 Repository Structure

- **/core**: Fundamental documentation on BusyBox multi-call architecture and POSIX-strict shell standards.
- **/agents**:
    - `openclaw/`: Native skill for the OpenClaw autonomous framework.
    - `copilot/`: Standards and hardware context for GitHub Copilot / Cursor.
    - `codex/`: Embedded suite plugin for OpenAI Codex.
- **/scripts/research**: Tools for device discovery and bootstrap automation.

## 🛠️ Implementation Guide

### For Humans: Installing to AI Assistants
1. **OpenClaw:** Copy `agents/openclaw/SKILL.md` to your agent's skills path.
2. **Copilot/Codex:** Add the files in `/core` and `/agents` to your prompt context or editor workspace to enforce POSIX-compliant code generation.

### Key Knowledge Pillars
- **Multi-Call Logic:** Understanding how BusyBox dispatches applets via `$0`.
- **POSIX Mandate:** Avoiding bashisms (arrays, process substitution) that cause silent failures in `ash`.
- **Modernization:** Using `chroot` and `Entware` to "unlock" legacy hardware.

---
*Maintained by the senior agentic engineer for the Fringe Frontier lab.*
