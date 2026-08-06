# Bible Context Research

A Codex/ChatGPT plugin for studying biblical books and passages in their historical, cultural, political, geographical, literary, linguistic, and ancient comparative contexts. It is designed to remain denominationally neutral and to distinguish textual evidence from historical reconstruction and scholarly inference.

## Included skill

`research-bible-context` supports 19 study modes, including full context reports, reading companions, authorship and dating, timelines, geography, ancient cultural comparisons, biblical connections, and common misunderstandings.

Examples:

- `Give me a reading companion for Numbers 1.`
- `16 - Trace the firstborn theme through Scripture.`
- `Show me the menu.`

## Original-language pronunciation

When Hebrew, Aramaic, or Greek materially improves a study, the skill can provide the original script, transliteration, concise written pronunciation, contextual meaning, and a verified Blue Letter Bible Strong's pronunciation link.

Native inline pronunciation controls are used only when the current environment supports them. Written guidance and the verified BLB link remain the fallback. The skill also distinguishes lexical links from multiword expressions, identifies relevant pronunciation traditions and uncertainty, and distinguishes יהוה (`YHWH`) from the traditional reading `Adonai`.

## Synchronization

The merged `main` branch is authoritative. Installed skills, Custom GPT instructions, ChatGPT project copies, and other downstream integrations do not update automatically and should be checked after repository changes.

## Install from this marketplace

Add this GitHub repository as a Codex plugin marketplace:

```bash
codex plugin marketplace add 7npftsjgc7-oss/bible-context-research
codex plugin add bible-context-research@bible-context-research
```

Restart Codex or begin a new conversation after installation so the skill is discovered.

## License

MIT
