# Lun Bian | "What the hand knows, the heart grasps."

> Turn your actions into a reusable Skill — no prompt writing required. Behavior capture → auto packaging, end to end.

---

## Origin

**"Lun Bian"** comes from *Zhuangzi: The Way of Heaven* (《庄子·天道》), an ancient Chinese classic (~300 BCE). Lun Bian was a wheelwright in the State of Qi during the Spring and Autumn period. Duke Huan asked why he never passed his craft to his son. He replied:

> *"What the hand knows, the heart grasps — but the mouth cannot speak it. There is a knack to it that cannot be put into words. I cannot teach it to my son, nor can he learn it from me."*

This is exactly the essence of this Skill: users need not write a single prompt. Just do it once, and the Skill learns from your actions.

---

## What It Does

**Lun Bian** is a meta-Skill that creates Skills. Three entry points, one pipeline:

| Entry | Scenario | What you'll hear |
|-------|----------|------------------|
| **Phase 1-A Behavior Capture** | You can't describe what you want, but can show it | "Start operating, say 'done' when finished" |
| **Phase 1-B Intent Description** | You know exactly what you need | "Got it. Here's the spec, review it" |
| **Polishing Entry** | You already have a Skill, want to optimize/publish | "Let's inspect — is this material worth carving?" |

## Six Forging Stages

```
Phase 0 Intake ──→ Phase 1 Understand ──→ Phase 2 Draft
                                               │
                                          Phase 2.5 Test ←── User feedback loop
                                               │
                                          Phase 3 Harden ←── Darwin self-evolution scoring
                                               │
                                          Phase 4 Polish ←── Luban showcase (README + certificate)
                                               │
                                          Phase 5 Package ←── Dep install + multi-platform packaging
```

## Quick Start

Just say:

```
"Help me create a skill that auto-organizes desktop files"
"I don't know how to describe it, watch what I do"
"Polish this skill"
"Turn my actions into a skill and publish to ClawHub"
```

Lun Bian auto-detects the entry point and runs the full 0-5 forging pipeline.

## Trigger Phrases

- `help me create a skill` / `create a skill` / `forge a skill`
- `polish this skill` / `optimize my skill`
- `turn my actions into a skill` / `turn these steps into a skill`
- `lun bian` / `skill forge` / `package and publish this skill`

## Key Capabilities

- **Behavior Capture**: 5-dimension observation (mouse trajectory, keyboard input, screen focus, operation rhythm, result feedback) via `analyze_image` + `shell_executor`
- **Darwin Self-Evolution**: 9-dimension scoring + ratchet retention (keep only if genuinely better) + max 2 rounds per dimension
- **Luban Polishing**: Inspect → Measure → Carve → Showcase → Deliver, with 3-level rollback mechanism
- **Multi-Platform Packaging**: GitHub + ClawHub + skills.sh + UUmit + universal .zip

## Forging Commandments (15 Rules)

1. User can't describe → auto-switch to behavior capture, never give up
2. Skip behavior confirmation → FORBIDDEN
3. Skip testing, jump to hardening → FORBIDDEN
4. Only one fix option during testing → FORBIDDEN (minimum 2)
5. No deviation log after test fix → FORBIDDEN
6. No showcase after hardening → FORBIDDEN
7. No packaging after showcase → FORBIDDEN
8. Self-evaluate self-improve → FORBIDDEN (must use independent sub-agent)
9. Silent dependency failure → FORBIDDEN
10. Bloat for higher score → FORBIDDEN
11. Leak credentials/private paths → FORBIDDEN
12. Hardcode single runtime → FORBIDDEN (must be runtime-neutral)
13. Superficial fix on user rejection → FORBIDDEN (deep deviation analysis required)
14. Destructive rollback (reset --hard) → FORBIDDEN
15. No status report after rollback → FORBIDDEN

## Mandatory Stop Points (11)

1. After each behavior inference round (Phase 1-A)
2. After draft completion, showing all files (Phase 2)
3. After each deviation analysis report (Phase 2.5)
4. After generating fix options, waiting for selection (Phase 2.5)
5. After executing fix, waiting for confirmation (Phase 2.5)
6. After baseline evaluation scorecard (Phase 3.1)
7. After each skill optimization round (Phase 3.2)
8. When proposing exploratory rewrite (Phase 3.3)
9. Before executing rollback (Phase 2.5 / Phase 4)
10. After packaging complete, showing release package (Phase 5)
11. Any high-risk operation

## Output Structure

For each forged Skill:

```
[skill-name]/
├── SKILL.md              # Core definition
├── README.md             # Full README + Showcase
├── test-prompts.json     # Test cases
├── results.tsv           # Darwin evolution history
├── scripts/              # Install & packaging scripts
├── assets/               # GIF + screenshots
└── skill-forge-export.zip
```

## Compatibility

Skills forged by Lun Bian are runtime-neutral, runnable on:
Claude Code / Codex / Cursor / OpenClaw / Hermes / Marvis / Workbuddy / Jiuwenswarm

## License

MIT. License of forged Skills is chosen by the creator.

---

*"What the hand knows, the heart grasps."*
