---
name: sanity-template-publishing
description: Enforce title and slug rules when publishing templates to Sanity. Use when creating or updating template documents in Sanity that have a title and slug, typically via your Sanity MCP tools.
---

# Sanity template publishing rules

Apply these rules with your own Sanity tools when writing a template document that has a title and slug.

- **Title case:** format `title` in Title Case, capitalizing the first word and all major words. Example: `Deep Search With Bright Data`.
- **Slug matches the title:** derive `slug` from the title by lowercasing it, replacing spaces with hyphens, and removing any character that is not a letter, number, or hyphen. Example: title `Deep Search With Bright Data` gives slug `deep-search-with-bright-data`.
