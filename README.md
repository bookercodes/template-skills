# template-skills

A collection of agent skills for building and publishing Mastra templates, installable with the [skills.sh](https://skills.sh/) CLI.

## Skills

- **mastra-template-readme**: Create or adapt `README.md` files for Mastra templates.
- **mastra-code-review**: Review and improve Mastra template code for correctness, teaching clarity, and a usable first run.
- **sanity-publishing**: Enforce title case and matching slug rules when publishing documents to Sanity.

## Installing

Install all skills into the current project:

```bash
npx skills add bookercodes/template-skills
```

List the available skills without installing:

```bash
npx skills add bookercodes/template-skills --list
```

Install a specific skill:

```bash
npx skills add bookercodes/template-skills --skill mastra-code-review
```

Target specific agents (omit to use detected agents, or use `'*'` for all):

```bash
npx skills add bookercodes/template-skills -a cursor -a claude-code
```

Install globally to your user directory instead of the current project:

```bash
npx skills add bookercodes/template-skills -g
```

## Updating

Check whether any installed skills have upstream changes:

```bash
npx skills check
```

Update by re-running `add`; the lock file (`skills-lock.json`) is rewritten to match:

```bash
npx skills add bookercodes/template-skills
```

Restore every skill exactly as recorded in the lock file, for teammates and CI:

```bash
npx skills experimental_install
```
