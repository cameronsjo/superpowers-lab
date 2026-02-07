# Superpowers Lab

Experimental skills for Claude Code Superpowers — new techniques and tools under active development.

> Maintained fork of [obra/superpowers-lab](https://github.com/obra/superpowers-lab) by [@cameronsjo](https://github.com/cameronsjo).

Functional but evolving skills that extend Claude Code's capabilities. May change based on real-world usage.

## Current Skills

### finding-duplicate-functions

Detect semantic code duplication in LLM-generated codebases. Unlike traditional copy-paste detectors that find syntactic duplicates, this skill identifies functions with the same intent but different implementations.

**Use cases:**
- Audit codebases that have grown organically with multiple contributors
- Identify utility functions that have been reimplemented multiple times
- Find consolidation opportunities before major refactoring
- Complement jscpd after syntactic duplicates are handled

**How it works:** Two-phase approach using classical function extraction followed by LLM-powered intent clustering. Haiku categorizes functions by domain, then Opus analyzes each category to find semantic duplicates.

See [skills/finding-duplicate-functions/SKILL.md](skills/finding-duplicate-functions/SKILL.md) for full documentation.

### mcp-cli

Use MCP servers on-demand via the `mcp` CLI tool. Discover and invoke tools, resources, and prompts without polluting context with pre-loaded MCP integrations.

**Use cases:**
- Query MCP servers without permanent configuration
- Explore available tools before deciding to integrate
- One-off MCP tool invocations

See [skills/mcp-cli/SKILL.md](skills/mcp-cli/SKILL.md) for full documentation.

### using-tmux-for-interactive-commands

Enables Claude Code to control interactive CLI tools (vim, git rebase -i, menuconfig, REPLs, etc.) through tmux sessions.

**Use cases:**
- Interactive text editors (vim, nano)
- Terminal UI tools (menuconfig, htop)
- Interactive REPLs (Python, Node, etc.)
- Interactive git operations (rebase -i, add -p)
- Any tool requiring keyboard navigation and real-time interaction

**How it works:** Creates detached tmux sessions, sends keystrokes programmatically, and captures terminal output to enable automation of traditionally manual workflows.

See [skills/using-tmux-for-interactive-commands/SKILL.md](skills/using-tmux-for-interactive-commands/SKILL.md) for full documentation.

## Installation

```bash
# Install the plugin
claude-code plugin install https://github.com/obra/superpowers-lab

# Or add to your claude.json
{
  "plugins": [
    "https://github.com/obra/superpowers-lab"
  ]
}
```

## Requirements

- tmux must be installed on your system
- Skills are tested on Linux/macOS (tmux required)

## Experimental Status

Skills in this plugin are:
- ✅ Functional and tested
- 🧪 Under active refinement
- 📝 May evolve based on usage
- 🔬 Open to feedback and improvements

## License

MIT License - see [LICENSE](LICENSE) for details.

## Support

- **Issues**: https://github.com/cameronsjo/superpowers-lab/issues
- **Upstream**: https://github.com/obra/superpowers-lab
