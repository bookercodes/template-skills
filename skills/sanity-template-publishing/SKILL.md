---
name: sanity-template-publishing
description: Enforce field rules when publishing templates to Sanity. Use when creating or updating a template document in Sanity, typically via your Sanity MCP tools.
---

# Sanity template publishing rules

Run this skill from the template's code folder so you can read the implementation and its README to fill these fields. Apply the rules with your own Sanity tools when writing a template document.

- **Title:** use the template's README title (its H1) exactly, so the two match.
- **Slug:** derive from the title by lowercasing it, replacing spaces with hyphens, and removing any character that is not a letter, number, or hyphen. Example: title `Company Brain with SurrealDB` gives slug `company-brain-with-surrealdb`.
- **Description:** write a short, compelling summary of what the template does. Example: `A shared team memory that recalls decisions, customer details, and company knowledge across conversations, with answers grounded in saved facts and documents.`
- **Long description:** always leave empty.
- **Code example:** always leave empty.
- **Agents:** list the names of the agents defined in the implementation.
- **Tools:** list the names of the tools defined in the implementation.
- **Use case:** choose the option that best fits the template. If none fits, choose `Other`.
