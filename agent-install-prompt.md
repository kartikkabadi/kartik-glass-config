# Agent Install Prompt

Send this to your local coding agent:

```text
Install the Kartik Glass Config from this repository.

Tasks:
1. Inspect my Zed and Ghostty config locations and identify the active files.
2. Install `zed/themes/kartik-glass-zed.json` into the Zed themes directory.
3. Merge `zed/settings-snippet.json` into my Zed settings without deleting unrelated settings.
4. Keep Zed `theme.mode` set to `system`.
5. Verify the Zed theme names exist:
   - Kartik Glass Light
   - Kartik Glass Dark
6. Install Ghostty files:
   - `ghostty/config.ghostty`
   - `ghostty/themes/Carbonfox-Black`
   - `ghostty/shaders/blaze.glsl`
7. Preserve my existing configs by backing them up or showing a diff before overwriting.
8. Validate JSON for Zed and check Ghostty config paths.
9. Report exactly what changed and whether either app needs a reload.

Do not read secrets, auth files, browser profiles, shell history, or unrelated dotfiles.
Do not overwrite unrelated settings.
```
