# Academic English Close Reading

A reusable skill for understanding academic and scientific English through precise sentence analysis.

## What it does

The skill follows this sequence:

**Chunk → Category → Head / Projection → Attachment → Function → Semantic role**

It distinguishes complements from adjuncts, separates constituency from dependency grammar, explains verb valency and prepositional phrases, and uses grammar trees and controlled rewrites to resolve ambiguous structures.

The teaching instructions are preserved from the original personal skill. Chinese explanations and natural Chinese translations are part of its default workflow. Ask explicitly for English or another language if preferred.

## Package contents

| Path | Purpose |
| --- | --- |
| `plugins/close-read-academic-english/plugin.json` | Portable skills-only plugin manifest |
| `plugins/close-read-academic-english/skills/close-read-academic-english/SKILL.md` | Complete teaching instructions |
| `plugins/close-read-academic-english/skills/close-read-academic-english/agents/openai.yaml` | Original skill display metadata |
| `plugins/close-read-academic-english/skills/close-read-academic-english/assets/icon.svg` | Original skill icon |
| `plugins/close-read-academic-english/assets/icon.svg` | Listing icon with 128 × 128 dimensions |
| `.agents/plugins/marketplace.json` | Repository marketplace catalog |

No MCP server, API key, external service, or bundled executable is required by this skill.

## Use the skill

In ChatGPT, mention `@close-read-academic-english`. In Codex, use `$close-read-academic-english` after installation. If installed through a plugin, select the skill or plugin from the client's available choices; its displayed identifier may be namespaced.

Example requests:

- “Analyze this sentence, separating category, attachment, function, and semantic role.”
- “In ‘depend heavily on temperature’, does ‘on temperature’ complement ‘depend’?”
- “Compare ‘sing in the room’ with ‘put the sample on the stage’.”
- “Only explain the attachment of this prepositional phrase.”
- “Use this skill, but answer entirely in English.”

## Repository distribution

Publish this repository on GitHub or mirror the same files to Gitee. People can inspect the instructions and obtain the package from the repository.

For clients supporting repository marketplaces, register this public GitHub repository:

```bash
codex plugin marketplace add Look001122/close-read-academic-english
```

To inspect or work with a local copy:

```bash
git clone https://github.com/Look001122/close-read-academic-english.git
```

Use the ChatGPT desktop app to select the **Academic English Tools** marketplace and install **Academic English Close Reading**. If the source is not visible, follow the current client refresh instructions in the official packaging guide. Availability varies by client.

[Official plugin packaging and marketplace guide](https://developers.openai.com/plugins/build/plugins)

## Public ChatGPT and Codex directory

A repository marketplace is a distribution source; it does not automatically create a public OpenAI directory listing.

For a public listing, submit the plugin directory `plugins/close-read-academic-english/` through OpenAI's plugin submission portal as a **Skills only** plugin. Archive that directory as a single plugin root when the portal requests an upload. Complete the publisher verification, required listing fields, and review process before publication.

The repository-level README and `.agents/plugins/marketplace.json` are outside the plugin root and should not be included in the skills-only submission archive.

[Official submission guide](https://developers.openai.com/plugins/deploy/submission)

## Verification

- The original personal skill passed the skill-creator frontmatter validation.
- Exported instructions, skill metadata, and icon are byte-identical to the original.
- Plugin and marketplace JSON were parsed, and local paths were checked.

The source package and repository marketplace are published on GitHub. This does not constitute an official OpenAI public directory listing; that route requires a separate verified-publisher submission and review.
