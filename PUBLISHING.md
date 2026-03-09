# Publishing Notes

## ClawHub publish

Verify auth:

```bash
clawhub whoami
```

Publish a new version:

```bash
clawhub publish /Users/donzurbrick/.openclaw/workspace/skills/battle-tested-agent \
  --slug battle-tested-agent \
  --name "Battle-Tested Agent" \
  --version 1.2.0 \
  --changelog "Public repo, MIT license, README improvements"
```

## Update existing listing

Bump `version:` in `SKILL.md`, then publish again with a matching changelog.

## Pre-publish checklist
- README is current
- LICENSE present
- `homepage` in `SKILL.md` points to public repo
- `license` in `SKILL.md` matches repo license
- scripts are executable
- no private workspace paths leaked into docs or examples

## Repo
- GitHub: https://github.com/zurbrick/battle-tested-agent
- ClawHub slug: `battle-tested-agent`
