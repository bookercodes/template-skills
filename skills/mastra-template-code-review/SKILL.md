---
name: mastra-template-code-review
description: Review and improve Mastra template code for correctness, teaching clarity, and a usable first run. Excludes README editing.
---

# Mastra template code review

Review implementation, configuration, and environment examples. Apply fixes when requested. Another skill handles README work.

## Teaching and code quality

Optimize for a TypeScript developer who may be new to Mastra and AI frameworks.

- Use the minimum readable code needed to achieve and explain the outcome.
- Prefer direct, linear, happy-path code.
- Assume expected inputs, configured environment variables, and available services.
- Avoid unnecessary guards, validation, retries, fallbacks, compatibility code, custom errors, and production infrastructure.
- Do not add abstractions for hypothetical reuse. Keep important behavior visible.
- Use descriptive names and realistic sample data. Introduce one primary idea at a time.
- Explain unfamiliar concepts where the learner encounters them.
- Follow repository style and the installed Mastra version. Verify APIs against installed documentation and types; load the Mastra skill when uncertain.
- Keep workflow steps focused on their stated purpose.
- Prefer inferred types over assertions that hide errors.
- Remove anything that distracts from the lesson unless production readiness is explicitly requested.

## Configuration

- Remove promotional language and unsupported claims from comments, prompts, and descriptions.
- Give environment variables concise comments explaining purpose, whether required, credential sources, and relevant defaults or allowed values.
- Use a current model suited to the task and budget. Verify its identifier and Mastra support before changing it.
- Ignore local credentials, databases and sidecar files, logs, dependencies, and build output. Keep `.env.example` tracked.

## First-run experience

Treat Mastra Studio as the primary demo surface.

- Give agents and workflows clear names and descriptions.
- Make it obvious what to select, what input to provide, and what output to expect.
- Choose a realistic first interaction that demonstrates the intended outcome.
- Test from a new user’s perspective, including the first Studio interaction when possible.

## Validation and delivery

Run type checks and a build after code changes. Test changed behavior where practical.

Report concrete changes, checks performed, and anything unverified. Compilation does not establish that a live run works.

Preserve unrelated changes and commit attribution. Commit or push only when authorized.
