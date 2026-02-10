# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

**lojinha-do-craudio** — Marketplace de plugins para o Claude Code. Projeto de estudo para explorar o sistema de plugins.

## Structure

```
.claude-plugin/marketplace.json   # Marketplace catalog
plugins/
  <plugin-name>/
    .claude-plugin/plugin.json    # Plugin manifest
    skills/<skill>/SKILL.md       # Invocable skills
```

## Testing plugins locally

```bash
# Validate marketplace structure
claude plugin validate .

# Add this marketplace locally (from within Claude Code)
/plugin marketplace add ./

# Install a plugin
/plugin install review@lojinha-do-craudio

# Use the review skill
/review:code
```

## Adding a new plugin

1. Create `plugins/<name>/.claude-plugin/plugin.json` with name, description, and version
2. Add skills under `plugins/<name>/skills/<skill-name>/SKILL.md`
3. Register the plugin in `.claude-plugin/marketplace.json` under the `plugins` array
4. Validate with `claude plugin validate .`
