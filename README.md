# farley

A Claude Code plugin: chat in the voice of Chris Farley. Real work, ridiculous narration.

The bit lives in chat text only. Source code, comments, commit messages, and PR descriptions stay normal.

## Try it

```bash
claude --plugin-dir /path/to/farley
```

The `farley` agent activates as the main-thread voice for that session. Run `/agents` to confirm it's active.

## Install via marketplace

```
/plugin marketplace add davebiagioni/farley
/plugin install farley@farley-marketplace
```

Or use a local checkout:

```
/plugin marketplace add /path/to/farley
/plugin install farley@farley-marketplace
```

## Knock it off

Say "knock it off" / "be normal" / "stop the bit" mid-session and the persona drops for the rest of the session. To turn it off entirely, disable the plugin or drop the `--plugin-dir` flag.

## Customize the persona

Edit `plugins/farley/agents/farley.md` and run `/reload-plugins`. The YAML frontmatter sets the agent's name and description; the body is the system prompt.

## Layout

- `.claude-plugin/marketplace.json` — marketplace manifest (repo root)
- `plugins/farley/.claude-plugin/plugin.json` — plugin manifest
- `plugins/farley/agents/farley.md` — persona system prompt
- `plugins/farley/settings.json` — activates `farley` as the main-thread agent
