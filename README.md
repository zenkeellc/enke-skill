# enke skills have moved

This repository has been split into two Claude Code skills, each in its own repository. This repo is kept only as a pointer — no code lives here anymore.

| Skill | What it does | Repository |
|-------|--------------|------------|
| **enke** | Short links, file sharing, landing pages, click analytics | [enke-link-skill](https://github.com/zenkeellc/enke-link-skill) |
| **enke-mem** | Persistent agent memory — remember/recall across sessions, knowledge-base docs (RAG) | [enke-mem-skill](https://github.com/zenkeellc/enke-mem-skill) |

Both skills require the en.ke CLI:

```bash
npm install -g enke-cli
enke login
```

## Install the link skill (enke)

```bash
git clone https://github.com/zenkeellc/enke-link-skill.git
mkdir -p ~/.claude/skills/enke
cp enke-link-skill/SKILL.md ~/.claude/skills/enke/
cp -r enke-link-skill/references ~/.claude/skills/enke/
```

Then ask Claude: "shorten this URL" / "帮我缩短这个链接".

## Install the memory skill (enke-mem)

```bash
git clone https://github.com/zenkeellc/enke-mem-skill.git
mkdir -p ~/.claude/skills/enke-mem
cp enke-mem-skill/SKILL.md ~/.claude/skills/enke-mem/
cp -r enke-mem-skill/references ~/.claude/skills/enke-mem/
```

Then ask Claude: "remember that..." / "记住...", or "recall..." / "回忆...".

> Tip: for reliable routing of remember/recall requests to en.ke (instead of Claude Code's built-in local memory), add the CLAUDE.md snippet from the [enke-mem-skill README](https://github.com/zenkeellc/enke-mem-skill#3-recommended-add-a-routing-rule-to-your-claudemd).

See each repository's README for full command references and configuration.

## License

MIT
