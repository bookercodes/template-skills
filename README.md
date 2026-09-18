# template-skills

A collection of agent skills, installable with the [skills.sh](https://skills.sh/) CLI.

## Skills

- **mastra-template-readme**: Create or adapt `README.md` files for Mastra templates.
- **mastra-template-code-review**: Review and improve Mastra template code for correctness, teaching clarity, and a usable first run.
- **sanity-template-publishing**: Enforce title case and matching slug rules when publishing templates to Sanity.
- **workshop-description-writer**: Write titles and event-page descriptions for Mastra workshops.

## Installing

Install all skills globally so they are available across all your projects:

```bash
npx skills add bookercodes/template-skills -g
```

List the available skills without installing:

```bash
npx skills add bookercodes/template-skills --list
```

Install a specific skill globally:

```bash
npx skills add bookercodes/template-skills --skill mastra-template-code-review -g
```

Target specific agents (omit to use detected agents, or use `'*'` for all):

```bash
npx skills add bookercodes/template-skills -g -a cursor -a claude-code
```

## Updating

Check whether any installed skills have upstream changes:

```bash
npx skills check
```

Update by re-running `add` globally; the lock file is rewritten to match:

```bash
npx skills add bookercodes/template-skills -g
```
