# Translator Agent

A Claude skill that turns Claude into a world-class translator and linguist. It handles translation between any language pair — living, endangered, classical, or constructed — with support for cultural adaptation, idiom handling, and multiple translation modes tuned to different use cases.

Built as a [Claude Skill](https://docs.claude.com) (`.skill` package) for use with Claude's computer use and file creation capabilities.

## What It Does

Rather than performing mechanical word-for-word substitution, this skill instructs Claude to translate **meaning** — preserving tone, register, cultural context, idiom, and authorial voice across languages. It also surfaces translator's notes when concepts don't map cleanly between languages.

## Translation Modes

| Mode | Use Case |
|---|---|
| **Faithful** | Legal, technical, academic, medical documents |
| **Natural** | Business communication, emails, general prose |
| **Literary** | Fiction, poetry, speeches, personal letters |
| **Idiomatic** | Marketing, advertising, colloquial text, humor |
| **Diplomatic** | Sensitive communications, negotiations, official statements |

You can specify a mode explicitly or let the agent infer the best fit from context.

## Language Coverage

Covers all major world languages and language families including European, Middle Eastern & Central Asian, South & Southeast Asian, East Asian, African, and Classical/Historical languages (Latin, Ancient Greek, Sanskrit, Classical Chinese, etc.). Creoles, constructed languages, and specialized registers are handled on a case-by-case basis.

## Output Structure

Each translation includes:

- **Translation** — the full translated text, matching the original document's structure.
- **Translator's Notes** *(when applicable)* — flags for untranslatable concepts, cultural adaptations, source ambiguities, register/tone decisions, and alternative renderings.
- **Fidelity Assessment** *(on request)* — a brief evaluation of how closely the translation tracks the original and where the most significant interpretive choices were made.

## Usage Examples

```
Translate this contract clause from German to English. Faithful mode.
Flag any legal terms that don't map cleanly.
```

```
I have a marketing tagline in English. Translate it into Brazilian Portuguese,
Japanese, and French. Idiomatic mode — I care about impact, not literal accuracy.
```

```
Translate this poem from Pablo Neruda's original Spanish.
Literary mode. I want to feel what a Spanish reader feels.
```

```
What language is this text in, and what does it say?
```

## Installation

1. Download `translator-agent.skill`.
2. Upload it to your Claude skill directory (typically `/mnt/skills/user/`).
3. The skill triggers automatically when you ask Claude to translate, identify a language, or perform cross-language adaptation.

## How It Works

The `.skill` file is a zip archive containing a `SKILL.md` — a structured prompt that defines the agent's role, behavior rules, translation modes, output format, and language coverage. Claude reads this at invocation time and adopts the described persona and workflow.

## License

MIT
