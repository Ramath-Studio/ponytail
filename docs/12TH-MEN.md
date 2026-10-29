# 12th Men — Ponytail install

Org-pinned fork of [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail) for Ramath-Studio repos.

## Cursor hooks (global or per project)

```bash
git clone https://github.com/Ramath-Studio/ponytail ~/.cursor/vendor/ponytail
node ~/.cursor/vendor/ponytail/scripts/cursor-hooks.js install
```

Per-repo hooks (keeps team on same checkout path if you vendor under the repo):

```bash
git clone https://github.com/Ramath-Studio/ponytail .vendor/ponytail
node .vendor/ponytail/scripts/cursor-hooks.js install --project
```

Default level: `PONYTAIL_DEFAULT_MODE=full` or `~/.config/ponytail/config.json` with `{ "defaultMode": "full" }`.

**Do not** also copy `.cursor/rules/ponytail.mdc` when hooks are active (double rules). See INSTALL.md § Cursor.

## Skills CLI (ponytail commands only)

```bash
npx skills add Ramath-Studio/ponytail --agent cursor -y
```

## Engineering skills in app repos

Install **code-review** and **diagnosing-bugs** at the **project** level (already committed under `.agents/skills/` in each 12th Men repo). Refresh from upstream:

```bash
npx skills add mattpocock/skills --skill code-review --skill diagnosing-bugs --agent cursor -p -y --copy
```

Then commit `.agents/skills/` changes. Standards: root `CLAUDE.md`; tracker setup: `/setup-matt-pocock-skills`.

## 12th Men repos

Same six services as in [cavemane/docs/12TH-MEN.md](https://github.com/Ramath-Studio/cavemane/blob/main/docs/12TH-MEN.md).
