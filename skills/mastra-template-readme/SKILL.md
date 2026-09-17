---
name: mastra-template-readme
description: Create or adapt README.md files for Mastra templates. Use when a user asks for a template README, template documentation, product description, quickstart, or launch copy for a Mastra example.
---

# Mastra template README

Write README files that explain Mastra templates as small, useful products. Lead with what the project does for its user. Follow the required format while preserving useful contributor ideas and voice.

## Workflow

1. Inspect the implementation and any existing README.
2. Establish the use case, first successful run, and template category.
3. Choose or preserve an appropriate title.
4. Create or adapt the README using the required structure.
5. Read the result as a first-time user and check it against the implementation.

Use context already available from the repository and conversation. Ask only for missing facts that materially affect the result.

If the user requests a draft for review, output it without editing files. A README request alone does not authorize installing this skill, committing changes, or publishing them.

## Understand the project before writing

Read the implementation before drafting the title or README. Treat the existing README as context to verify, not the source of truth.

Inspect:

- `package.json`, lockfiles, and `.env.example` for commands, dependencies, package manager, and required services.
- Agent instructions, workflows, and tools for actual behavior.
- Sample data and example inputs for the intended use case.
- Outputs, human approval steps, and limitations visible in the implementation.
- Contribution documentation and repository information for maintenance and publisher context.

Establish:

- Who uses the project and what they want to accomplish.
- What they provide as input.
- What the agent or workflow does, including external integrations.
- What useful result they receive.
- What the implementation supports today versus what is merely suggested.
- Which environment variables are required, what they mean, and where their values come from.
- Which preparation commands are necessary before starting the application.
- The template slug, setup commands, Studio agent or workflow name, and a concrete first interaction.

Do not infer the product solely from its repository name, dependencies, or existing marketing copy. Use the implementation to inform the title, opening, and examples.

Ask about motivation, intended audience, or publisher category only when inspection and conversation do not establish them. Do not require a fixed number of intake questions.

## Identify the template category

Determine the category from repository evidence and confirmed user context:

- **Official:** maintained as an official template in the Mastra monorepo. A standalone repository may be a synchronized distribution.
- **Partnership:** contributed through an identified partnership to show how Mastra works with the partner’s product or service. Maintained in its own repository.
- **Community:** contributed independently by a person or organization. Maintained in its own repository.

Use the conversation and project framing together to establish the category. A user-confirmed partnership is sufficient; do not ask them to confirm it again. A title using the partnership format (`<Use case> with <Partner>`) is a meaningful signal when it is consistent with the integration and contributor context. Do not require an additional formal declaration when that context already makes the category clear. A dependency or company-owned repository alone is not enough.

Treat existing About sections and contribution guides as fallible project content. They may contain copied official-template boilerplate. Monorepo or synchronization language must not override established partner or community context. When a standalone partner repository contains that boilerplate, correct the README attribution and direct contributions to its canonical repository unless a valid partner-specific guide is available.

“Contractor” describes the contributor’s relationship, not the template category.

Ask about category, contributor name, or contribution destination only when the conversation and repository context leave a material ambiguity. Ask only for the unresolved fact, continue independent edits, and do not reopen facts the user has settled.

## Create or adapt the README

### When there is no README

Create one from scratch using the implementation, sample data, and confirmed contributor context. Follow the required structure and title rules.

### When a README already exists

Adapt it to the required format while preserving the contributor’s voice, ideas, and useful project-specific content.

An existing README may have been written by a partner or community contributor. Treat it as a contribution to edit thoughtfully, not text to replace wholesale. Its existence does not establish the template category.

Before editing, identify:

- Product framing and motivation.
- Distinctive wording or tone worth retaining.
- Examples, explanations, and customization ideas.
- Setup instructions, environment-variable explanations, limitations, and relevant links.
- Additional sections outside the required structure.

Map existing content into the required sections. Move explanations of credentials, environment variables, and external service access into Prerequisites. Keep Quickstart focused on the actions needed to run the project.

Restructure and trim where necessary, but do not rewrite accurate prose merely to make it sound like your own writing.

The format is strict; the voice does not need to be uniform. Preserve personality and concrete ideas while correcting unsupported claims, unclear wording, and marketing language.

### Additional sections

Retain useful contributor-added sections that do not fit naturally inside the required structure.

Move them toward the bottom, after Customization and immediately before About Mastra templates. Preserve their H2 headings and relative order when practical.

Examples include detailed integration explanations, deployment instructions, troubleshooting, and project-specific design decisions. The Demo section, when present, is not a contributor-added section and must remain directly after Why we built this.

Keep information essential to the first successful run in Prerequisites or Quickstart. Do not bury required setup in a relocated section.

Preserve actionable prompts and experiments in Try it out, immediately after Quickstart.

Merge duplicated content. Remove sections only when inaccurate, obsolete, redundant, or outside the README’s purpose, not merely because they are absent from the standard outline.

About Mastra templates remains the final section.

## Ideate the title

Choose the H1 after understanding the implementation.

The title should be concise, clear, and recognizable. It should signal what the template helps someone do without relying on the opening paragraph to explain the name.

Prefer a familiar use-case name when accurate, such as “Deep Search,” “Customer Support,” or “Meeting Notes.” Do not force the project into a familiar category that misrepresents its behavior.

Consider a few candidates:

- A familiar name for the use case.
- A direct description of the task or outcome.
- An established product name supplied by the user or contributor.

Evaluate candidates for accuracy, familiarity, and brevity. Avoid vague metaphors, invented branding, and titles that pack in a feature list.

Choose the strongest title when the evidence is clear. Present a shortlist only when requested or when materially different framings need the user’s judgment. Preserve an explicitly chosen title unless asked to revisit it.

### Title format

Format the title in Title Case, capitalizing the first word and all major words. Keep minor words such as `with`, `and`, and `for` lowercase unless they are the first word.

- **Official or community:** `# <Clear use-case or product name>`
- **Partnership:** `# <Clear use-case or product name> with <Partner name>`

For example:

- `# Deep Search`
- `# Company Brain with SurrealDB`

Use the verified partner name. Do not hard-code a particular partner into unrelated templates.

Do not add “AI,” “agent,” “template,” or “Mastra” merely as decoration. Include technical terms only when they help identify the use case.

## Writing principles

- Avoid em dashes. Use a colon to introduce an explanation, or use a comma, parentheses, or a separate sentence as appropriate. In Prerequisites, follow each linked bold credential label with a colon.
- Write for engineers and technical product managers evaluating whether to try the template.
- Explain inputs, behavior, and useful results before implementation details.
- Use factual, concrete language throughout, including partnership attribution and contributor-added sections.
- Avoid marketing language: promotional adjectives, superlatives, vague benefits, and unsupported claims.
- Avoid phrases such as “powerful,” “seamless,” “cutting-edge,” “revolutionary,” “unlocks,” and “showcases the power of AI.”
- Explain what a partner’s integration does rather than advertising the partner.
- Avoid repeatedly saying “This template demonstrates.”
- Do not present intended or untested behavior as verified.
- Preserve distinctive, accurate contributor language.
- Prefer concise bullets for requirements, configuration explanations, actions, and examples.
- Keep ordinary paragraphs short.
- Explain architecture only when it helps users configure, operate, or adapt the project.
- Do not invent motivation, customer anecdotes, credentials, integrations, or outcomes.

Preserving contributor voice does not require preserving hype. Prefer “uses <service> to search company documents” over “unlocks powerful knowledge discovery.”

## Markdown formatting

Use standard Markdown headings for sections. Never use a bold bullet such as `- **Customization**` as a section title.

- Use one H1 for the product title.
- Use H2s for the main sections.
- Write paragraphs directly beneath headings, without indentation.
- Use ordinary bullets for prerequisites, examples, and customization ideas.
- Use a numbered list for Quickstart, with bold step labels and nested instruction bullets.
- Only indent content when it belongs inside a list item.
- Keep blank lines between headings, paragraphs, and lists.
- Use inline code for short commands.
- Avoid standalone “Run:” paragraphs and fenced command blocks when a concise instruction bullet is sufficient.
- Use code blocks when genuinely needed for multiline content or syntax that would be difficult to read inline.
- Do not add emoji beyond the rocket in the Quickstart heading.

The preference for bullets applies to content that is naturally a list. It does not apply to section titles or ordinary paragraphs.

## Required README structure

Use this order unless the user explicitly requests otherwise:

1. H1 title and opening paragraph.
2. Why we built this.
3. Demo, when a demo video is available.
4. Prerequisites.
5. Quickstart.
6. Try it out.
7. Customization.
8. Useful contributor-added sections, if present.
9. About Mastra templates.

Do not include a separate Features section. Explain capabilities through actionable examples in Try it out.

The example below includes a preparation step. Omit it when unnecessary or replace it with the preparation the project actually requires. Add further steps when needed.

```markdown
# <Product name, including partner when applicable>

<One short paragraph describing what the product accepts, what it does,
and the useful result.>

## Why we built this

<A short explanation of the practical problem or observation behind
the product.>

## Demo

<video controls width="640" height="360" src="<verified Cloudinary video URL>"></video>

## Prerequisites

- **[<Model provider> API key](<verified credential URL>)**: set `<ENV_VARIABLE>` to authenticate the default model.
- **[<Service> credentials](<verified access URL>)**: <what the service provides>. Set `<ENV_VARIABLE>` to <required value>.
- <Additional concise configuration or access details needed for the first run.>

## Quickstart 🚀

1. **Clone the template**
   - Run `npx create-mastra@latest --template <template-slug-or-repository-url>` to scaffold the project locally.
   - <Include the correct directory change when needed.>
2. **Add your API keys**
   - Run `cp .env.example .env` and fill in the values described under Prerequisites.
3. **<Required preparation, such as Seed the database>**
   - Run `<actual preparation command>` to <brief purpose>.
4. **Start the dev server**
   - Run `<package-manager> run dev`.
   - Open [Mastra Studio](http://localhost:4111), select **<agent or workflow>**, and <exact first action>. <Expected result.>

## Try it out

- <Concrete prompt or experiment and the behavior to look for.>
- <Another action that illustrates a useful capability.>
- <Another supported scenario.>

## Customization

- Open the project in your coding agent and describe what you want to change. For example: “<Specific customization relevant to this template>. Explore the code and propose a plan before making changes.”
- <A second concrete adaptation involving data, integrations, or behavior.>

## <Useful contributor-added section, if present>

<Preserved project-specific content.>

## About Mastra templates

<Category-specific description and attribution.>

[Want to contribute?](<verified contribution URL>)
```

Replace placeholders with verified project details. Do not include an empty additional section or unnecessary preparation step. Omit the Demo section entirely when no demo video is available.

## Section rules

### Opening

The opening must stand alone. Explain what goes in, what the product does, and what comes out.

Make the use case clear enough for readers to evaluate the project before reaching the examples.

Mention Mastra or implementation details only when they help orient the reader. Do not make the opening a dependency list.

### Why we built this

Explain the practical problem or observation behind the product and why solving it is useful.

Preserve an existing contributor’s motivation where supported. Do not turn the section into a feature inventory or invent a personal origin story.

### Demo

Include the Demo section only when a demo video is available. When present, use the exact heading `## Demo` immediately after `## Why we built this` and before `## Prerequisites`.

Embed the demo with an HTML `video` tag using fixed dimensions and playback controls:

```html
<video controls width="640" height="360" src="https://res.cloudinary.com/mastra-assets/video/upload/v1789407162/bright-data-agent-demo_1_iclc5b.mp4"></video>
```

Use the Cloudinary video URL supplied by the user or verified in the repository. Do not substitute another video host.

When no video is available, omit the Demo section entirely, including its `## Demo` heading. Do not add a placeholder, silently reuse a video from an unrelated template, or guess a Cloudinary URL. When a demo is expected but the URL is not yet available, ask the user for the Cloudinary URL when practical rather than leaving a placeholder.

### Prerequisites

Use `## Prerequisites` immediately before Quickstart.

Explain required credentials, external services, environment variables, and relevant account configuration here, not in Quickstart.

Use concise bullets. Group related variables by provider or service rather than creating an exhaustive reference table.

Make the bold credential or service label before the colon a clickable link to where users can obtain access:

- **[<Model provider> API key](<verified credential URL>)**: set `<API_KEY_VARIABLE>` for the default model.
- **[<Service> credentials](<verified access URL>)**: set `<ENDPOINT_VARIABLE>`, `<CONTEXT_VARIABLE>`, and `<API_KEY_VARIABLE>` using the values supplied by the service.

Include:

- The exact environment-variable names needed for the first run.
- What each value represents and where it comes from.
- Required account configuration, such as model access, permissions, or a service region.
- Relevant defaults or optional overrides when they materially affect setup.

Use additional bullets when helpful. Do not force several distinct requirements into a dense paragraph. Keep optional settings clearly distinguished from required values.

Prefer direct API-key, account-access, or signup pages over general homepages. Use the company or product page when it is the appropriate entry point for obtaining access.

Resolve links as follows:

- Reuse a relevant, verified URL from the repository or conversation.
- For a clearly identified provider such as OpenAI or Anthropic, look up the official credential page rather than asking the user.
- When a credential is project-specific or the service or access route is ambiguous, ask the user for the correct URL.
- Do not guess URLs or insert placeholder links into the finished README.

Explain requirements factually. Do not add promotional descriptions or unrelated warnings.

Do not list Node.js, npm, pnpm, or runtime and package-manager version requirements in the README. This documentation convention does not authorize changing package metadata or engine constraints.

Use the actual model provider and integrations. Do not copy example services into a template that does not use them.

Mention model substitution only when supported, and clarify that a different provider may require different credentials.

### Quickstart

Use the exact heading `## Quickstart 🚀`.

Write an ordered list with bold step names and concise nested instruction bullets. Steps are list items, not H3 headings.

The usual sequence is:

1. Clone the template.
2. Add your API keys.
3. Start the dev server.

This is a baseline, not a fixed step count. Add separate numbered steps for required preparation, in dependency order.

For example, a template that requires seeding should use:

1. **Clone the template**
2. **Add your API keys**
3. **Seed the database**
4. **Start the dev server**

Use the most accurate action label for the project, such as “Load the sample documents,” “Run migrations,” or “Seed the database.” Do not hide a distinct required action inside “Start the dev server” merely to keep three steps.

Keep the distinction clear:

- **Prerequisites:** what users need, what configuration values mean, and where to obtain them.
- **Quickstart:** the commands and actions that get the project running.

Additional nested bullets are welcome when they make an action easier to follow. Avoid lengthy explanatory paragraphs.

Quickstart rules:

- Use `npx create-mastra@latest --template <template>` with the correct template reference.
- For official templates in the Mastra monorepo, use the template slug, such as `npx create-mastra@latest --template text-to-sql`.
- For templates maintained in their own repository (partnership and community), use the full GitHub repository URL, such as `npx create-mastra@latest --template https://github.com/mastra-ai/template-surrealdb`.
- Do not include a project name argument. Prefer `npx create-mastra@latest --template text-to-sql` over `npx create-mastra@latest my-company-brain --template template-surrealdb-company-brain`.
- Ensure `cd` matches the directory actually created.
- Detect the package manager from repository evidence and use it consistently.
- Do not add a direct `git clone` alternative.
- Include copying `.env.example` to `.env`, then refer to Prerequisites for the values.
- Do not repeat provider descriptions or environment-variable explanations.
- Include every preparation command needed for the documented first run.
- End with the exact Studio agent or workflow, a realistic input, and an expected result supported by the example.
- If the template does not run in Studio, give its actual shortest path to a useful result.

Give one first-run action, then direct readers to Try it out for further exploration. If that section already contains the first-run example, reference it rather than repeating its full instructions.

### Try it out

This section replaces Features. Do not include a separate Features section.

Place it immediately after Quickstart, when the reader has the project running.

Use three to five bullets that explain capabilities through concrete actions: a prompt to send, data to supply, a correction to make, or an experiment to run.

Each bullet should explain what to do and what result or behavior to look for. Express these naturally; do not create repetitive “Action” and “Result” labels.

Preserve useful contributor-written examples and their voice. Keep specific prompts, memorable explanations, and meaningful experiments where supported.

Ground examples in the implementation and sample data. Be precise about which data is changed or preserved, and avoid promising behavior the code does not support.

Avoid abstract capability lists, long walkthroughs, and repetition of the Quickstart example.

### Customization

Use about two bullets.

The first should introduce using a coding agent to customize the template. Suggest describing the desired outcome and asking the agent to explore the code and propose a plan before making changes.

Include a concrete example prompt relevant to the project. Avoid generic prompts such as “make this better” and do not imply customization will work without review.

The second should offer another specific adaptation, such as replacing sample data, connecting a company source, changing a policy, or adjusting output behavior.

Mention file paths only when they help locate the customization.

### About Mastra templates

Tailor the entire section to the established category. Only official templates should mention the Mastra monorepo or synchronization process.

Use the appropriate pattern below, adapting it to verified facts.

**Official:**

```markdown
## About Mastra templates

This is an official Mastra template. Official templates live in the
[Mastra monorepo](<verified URL>) and are synchronized to standalone
repositories.

[Want to contribute?](<verified templates contributing guide>)
```

Include the synchronization statement only when confirmed by contribution documentation.

**Partnership:**

```markdown
## About Mastra templates

This partnership template was contributed by <partner> to show how
Mastra works with <product or service> for <concrete use case>.

[Want to contribute?](<partner contribution guide or canonical repository>)
```

**Community:**

```markdown
## About Mastra templates

This community template was contributed by <person or organization>
to show how Mastra can <concrete use case, including relevant tools
or integrations>. Community templates live in their own repositories.

[Want to contribute?](<community contribution guide or canonical repository>)
```

For partnership and community templates, explain the practical ecosystem connection: what users can do with Mastra and the tools involved. Prefer a specific integration or outcome over a generic claim about the “broader ecosystem.”

Keep attribution factual. Do not advertise the contributor or partner.

Do not describe community contributors as partners without an established relationship. Do not direct independently maintained templates to the Mastra monorepo for contributions.

Prefer the repository’s own contribution guide when it matches the established category and actual maintenance destination. If it contains conflicting monorepo boilerplate, link the canonical partner or community repository instead. Do not carry that boilerplate into the About section or block the README update on it. Editing the contribution guide itself is a separate scope decision.

## Final check

- The implementation was inspected before choosing the product framing.
- The H1 is concise, accurate, and signals a recognizable use case or task.
- The H1 title is in Title Case.
- Partnership titles follow `<Name> with <Partner name>`.
- The opening explains inputs, behavior, and results.
- Existing contributor voice, useful ideas, examples, and caveats are preserved.
- Section titles use headings, never bold list items.
- Ordinary paragraphs are not indented.
- When a demo video is available, `## Demo` appears directly after `## Why we built this`; otherwise the section is omitted.
- When present, the Demo section uses a `video` tag with `controls`, `width="640"`, `height="360"`, and a verified Cloudinary URL.
- When no demo video is available, the Demo section and its heading are omitted, with no placeholder left behind.
- Prerequisites is an H2 immediately before `## Quickstart 🚀`.
- Credential and service labels link to verified access pages and are followed by colons.
- The README contains no em dashes.
- Ambiguous access URLs were resolved with the user rather than guessed.
- Required environment variables and their meanings are explained in Prerequisites.
- Runtime and package-manager version requirements are omitted from the README.
- Quickstart uses numbered steps with bold labels and concise nested bullets.
- Required preparation has its own step when it is a distinct action.
- The number of steps follows the project’s needs rather than a fixed limit.
- Commands, slug, destination directory, variables, and Studio names match the project.
- Quickstart refers to Prerequisites rather than repeating credential explanations.
- There is no direct-clone alternative.
- The first interaction includes a supported expected result.
- Try it out follows Quickstart and explains capabilities through actionable examples.
- There is no separate Features section.
- The first customization bullet introduces planning changes with a coding agent.
- Useful additional sections sit after Customization and before About Mastra templates.
- The template category and contributor follow established conversation and project context; copied contribution boilerplate has not overridden them.
- Monorepo language appears only for official templates.
- Contribution links point to where the template is maintained.
- About Mastra templates is the final H2 section.
- Marketing language is absent throughout, including attribution and preserved additional sections.
- Markdown lists and indentation render correctly.
