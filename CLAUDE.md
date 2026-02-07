# Superpowers Lab - Fork Maintenance

## Fork Relationship

- **Origin (push)**: `cameronsjo/superpowers-lab`
- **Upstream (pull)**: `obra/superpowers-lab`

## Syncing Upstream

```bash
git fetch upstream
git merge upstream/main
```

Experimental repo — new skills may appear upstream. Review before merging.

## Where Customizations Live

- `README.md` — re-owned header
- `CLAUDE.md` — this file (fork-only)
- Skill modifications in `skills/`

## What Not to Touch When Merging

- New upstream skills — accept and review, don't auto-reject
- `.claude-plugin/plugin.json` version bumps — accept upstream
