# Agent Install Prompt

Send this to your local coding agent:

```text
Install the Codex Cursor Glass Zed theme from this repository.

Tasks:
1. Inspect my Zed config directory and confirm the active settings path.
2. Copy `themes/codex-cursor-glass.json` into the local Zed themes directory.
3. Merge `zed-settings-snippet.json` into my Zed `settings.json` without deleting unrelated settings.
4. Keep `theme.mode` set to `system` so Zed follows the OS light/dark appearance.
5. Verify the selected theme names exist in the theme file:
   - Codex Cursor Glass Light
   - Codex Cursor Glass Dark
6. Check whether the optional Charmed Icons extension is installed. If it is not installed, either remove the `icon_theme` block or tell me how to install it.
7. Validate JSON after editing.
8. Report exactly what changed and whether Zed needs a restart or reload.

Do not read secrets, auth files, browser profiles, or unrelated dotfiles.
Do not overwrite my existing settings. Merge only the relevant Zed theme settings.
```
