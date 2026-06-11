# Triage labels

Five canonical labels used by the `triage` skill:

| Label | Role |
|-------|------|
| `needs-triage` | Maintainer needs to evaluate |
| `needs-info` | Waiting on reporter for more detail |
| `ready-for-agent` | Fully specified; an AFK agent can pick it up |
| `ready-for-human` | Needs human implementation |
| `wontfix` | Will not be actioned |

These labels must exist in the GitHub repo. Create them with:

```bash
gh label create "needs-triage" --description "Needs triage by a maintainer"
gh label create "needs-info" --description "Waiting on reporter for more information"
gh label create "ready-for-agent" --description "Fully specified and ready for an agent"
gh label create "ready-for-human" --description "Ready for human implementation"
gh label create "wontfix" --description "Will not be actioned"
```

## State machine

An issue flows through these states:

1. **New** → `needs-triage`
2. **Insufficient detail** → `needs-info`
3. **Fully specified, agent-friendly** → `ready-for-agent`
4. **Needs human** → `ready-for-human`
5. **Rejected** → `wontfix`
