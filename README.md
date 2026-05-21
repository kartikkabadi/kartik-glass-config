# Codex Cursor Glass for Zed

A small Zed setup for a Codex/Cursor-inspired liquid glass look.

It includes:

- a local Zed theme file with matching dark and light variants
- system-theme switching for macOS light/dark mode
- a blue typing cursor in both modes
- a copy-paste prompt you can give to an agent to install and verify it

## Preview

This repository does not include screenshots yet. The theme is tuned for a neutral, glassy editor surface:

- Dark mode: charcoal glass, soft blue accents, balanced teal/green syntax
- Light mode: off-white glass, matching accent families with stronger contrast
- Both modes: consistent opacity on major surfaces to avoid blocky panels

## Files

- `themes/codex-cursor-glass.json`: the Zed theme
- `zed-settings-snippet.json`: the settings block to add to your Zed config
- `agent-install-prompt.md`: a prompt you can send to Codex, Cursor, OpenCode, or another local coding agent

## Manual Install

1. Open your Zed config directory.

   On macOS, it is usually:

   ```sh
   ~/.config/zed
   ```

2. Copy the theme file:

   ```sh
   mkdir -p ~/.config/zed/themes
   cp themes/codex-cursor-glass.json ~/.config/zed/themes/codex-cursor-glass.json
   ```

3. Merge this into `~/.config/zed/settings.json`:

   ```json
   {
     "theme": {
       "mode": "system",
       "light": "Codex Cursor Glass Light",
       "dark": "Codex Cursor Glass Dark"
     }
   }
   ```

4. Restart Zed or run `Reload Window`.

## Recommended Settings

This is the full snippet used with the theme:

```json
{
  "icon_theme": {
    "mode": "system",
    "light": "Light Charmed Icons",
    "dark": "Soft Charmed Icons"
  },
  "theme": {
    "mode": "system",
    "light": "Codex Cursor Glass Light",
    "dark": "Codex Cursor Glass Dark"
  }
}
```

The icon theme names come from the `charmed-icons` Zed extension. If you do not use that extension, remove the `icon_theme` block or choose your own icons.

## Agent Prompt

Use this prompt with a local coding agent:

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

## GitHub Setup Checklist

If you publish your own fork or variant, check:

- The theme JSON validates with `jq empty themes/codex-cursor-glass.json`.
- The README does not include machine-local paths except generic examples like `~/.config/zed`.
- No personal Zed settings, prompts databases, logs, or extension caches are committed.
- The repo has a license.
- The install instructions do not use `curl | sh` or any remote script execution.

## Notes

This is a personal taste theme, not an official Codex, Cursor, or Zed theme.
