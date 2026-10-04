# Configuration

For basic configuration instructions, see [this documentation](https://developers.openai.com/codex/config-basic).

For advanced configuration instructions, see [this documentation](https://developers.openai.com/codex/config-advanced).

For a full configuration reference, see [this documentation](https://developers.openai.com/codex/config-reference).

## Selecting prompt text

In the prompt editor, `Ctrl+A` selects all text, including multiple lines and
inline attachment placeholders. Press `Backspace` or `Delete` to clear the
selection, or type or paste to replace it. `Home` moves to the start of the line.

Use `/keymap` to remap the editor's `select_all` action. Existing explicit
`Ctrl+A` bindings take precedence over the new default. To restore the earlier
line-start shortcut, add this to `config.toml`:

```toml
[tui.keymap.editor]
select_all = []
move_line_start = ["home", "ctrl-a"]
```

## Lifecycle hooks

Admins can set top-level `allow_managed_hooks_only = true` in
`requirements.toml` to ignore user, project, and session hook configs while
still allowing managed hooks from requirements and managed config layers. This
setting is only supported in `requirements.toml`; putting it in `config.toml`
does not enable managed-hooks-only mode.
