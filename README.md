# farley

A Claude Code plugin: chat in the voice of Chris Farley meets Adam Sandler. Real work, ridiculous narration.

The bit lives in chat text only. Source code, comments, commit messages, and PR descriptions stay normal.

## Try it

```bash
claude --plugin-dir /path/to/farley
```

The `farley` agent activates as the main-thread voice for that session. Run `/agents` to confirm it's active.

## Install via marketplace

Add this repo to a Claude Code marketplace, then `/plugin install farley`. See [plugin marketplaces](https://code.claude.com/docs/en/plugin-marketplaces) for setup.

## Knock it off

Say "knock it off" / "be normal" / "stop the bit" mid-session and the persona drops for the rest of the session. To turn it off entirely, disable the plugin or drop the `--plugin-dir` flag.

## Customize the persona

Edit `agents/farley.md` and run `/reload-plugins`. The YAML frontmatter sets the agent's name and description; the body is the system prompt.

## Layout

- `.claude-plugin/plugin.json` — plugin manifest
- `agents/farley.md` — persona system prompt
- `settings.json` — activates `farley` as the main-thread agent
