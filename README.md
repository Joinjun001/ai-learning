# ai-learning

A version-controlled 1:1 learning system for persistent learner modeling, reusable teaching skills, subject knowledge state, and session summaries.

## Core idea

- **ChatGPT Project**: interactive learning workspace
- **SSalMuk Plugin**: reads/writes the working copy and performs Git operations
- **This repository**: source of truth for learner preferences, teaching skills, subject state, and compact session history

The prompt should stay short. Persistent state belongs in files.

## Session lifecycle

```text
Bootstrap
  -> Orientation
  -> Probe
  -> Plan
  -> Teach
  -> Quiz
  -> Persist
  -> Commit / Push
```

## Start a session

A short invocation is enough:

```text
@SSalMuk-Plugin ai-learning 암호학 이어서 공부하자
```

The agent should then follow `BOOTSTRAP.md` and `SYSTEM.md`.

## Repository structure

```text
.
├── BOOTSTRAP.md
├── SYSTEM.md
├── learner/
│   └── LEARNER.md
├── skills/
│   ├── common/
│   └── subjects/
├── subjects/
│   └── cryptography/
│       ├── STATE.json
│       ├── MAP.md
│       └── materials/
├── sessions/
│   ├── TEMPLATE.md
│   └── cryptography/
└── schemas/
    └── state.schema.json
```

## Data policy

This repository is public. Store only learning-related information that is safe to publish.

Do **not** commit:

- raw private conversations
- credentials, tokens, account identifiers
- private documents or copyrighted course PDFs
- unrelated personal information
- sensitive personal data

Prefer compact evidence and session summaries over raw logs.
