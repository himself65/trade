# Trade

> [!WARNING]
> This project is for educational and informational purposes only. Nothing here constitutes financial advice. Always do your own research and consult a qualified financial advisor before making investment decisions.

A personal Claude Code plugin marketplace housing one options-trading skill — backed by a curated library of 15 pitfalls and prior case studies (INTC, Mag-7, APP). Layout follows the [`himself65/finance-skills`](https://github.com/himself65/finance-skills) convention.

## Quick Start

### Claude Code — Install the plugin

```bash
npx plugins add himself65/trade-skills
```

### Claude Code — Install just the skill

```bash
npx skills add himself65/trade-skills
```

### Other agents

```bash
npx skills add himself65/trade-skills -a <agent-name>
```

### Local development install (from a clone)

```bash
git clone https://github.com/himself65/trade-skills.git ~/trade-skills
ln -s ~/trade-skills/plugins/trade/skills/trade ~/.claude/skills/trade
```

## Available Skills

### Trade (`trade`)

Multi-leg options trading assistant with concrete strikes, IV-aware structures, and probability-weighted scenarios.

| Skill | Description |
|---|---|
| [trade](plugins/trade/skills/trade/) | Options trading knowledge base — 15 pitfalls + INTC / Mag-7 / APP case studies + structure-to-regime framework. Lazy-loaded. |

## License

MIT
