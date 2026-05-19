

# Decisions

Last Updated: 2026-05-18

## Infrastructure
- Hermes runs persistently on VPS inside tmux
- Codex is the code execution layer
- OpenRouter powers Hermes
- OpenAI Platform API powers Codex
- VPS is primary execution environment

## Build Philosophy
- Demo first engineering
- Preserve future phase visibility
- Build incrementally
- Keep changes reversible
- Hardening before expansion

## Governance
- Hermes orchestrates
- Codex executes
- Dee approves strategic direction
- Escalations only for risk, revenue, architecture, or timeline impact

## Messaging
- Discord selected as operational control plane
- Notifications should be batched and low noise

## Memory
- Obsidian is the operational memory layer
- Current state documents remain authoritative

## Timeline
- Demo target: 2026-05-23
- Hermes operates 24/7 to hit this deadline
- Phase 1 must be complete before GC prospect demo