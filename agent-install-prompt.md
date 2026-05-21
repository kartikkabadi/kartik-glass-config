# Agent Install Prompt

Copy and send this whole prompt to a local agent:

```text
Install Kartik Glass Config for my editor and terminal.

Source repository:
https://github.com/kartikkabadi/kartik-glass-config

Files to use:
- Zed theme: zed/themes/kartik-glass-zed.json
- Zed settings snippet: zed/settings-snippet.json
- Ghostty config: ghostty/config.ghostty
- Ghostty theme: ghostty/themes/Carbonfox-Black
- Ghostty shader: ghostty/shaders/blaze.glsl

Tasks:
1. Fetch or clone the repository above into a temporary/local working folder.
2. Inspect my Zed and Ghostty config locations and identify the active files.
3. Install `zed/themes/kartik-glass-zed.json` into the Zed themes directory.
4. Merge `zed/settings-snippet.json` into my Zed settings without deleting unrelated settings.
5. Keep Zed `theme.mode` set to `system`.
6. Verify the Zed theme names exist:
   - Kartik Glass Light
   - Kartik Glass Dark
7. Install Ghostty files:
   - `ghostty/config.ghostty`
   - `ghostty/themes/Carbonfox-Black`
   - `ghostty/shaders/blaze.glsl`
8. Preserve my existing configs by backing them up or showing a diff before overwriting.
9. Validate JSON for Zed and check Ghostty config paths.
10. Report exactly what changed and whether either app needs a reload.

Do not read secrets, auth files, browser profiles, shell history, or unrelated dotfiles.
Do not overwrite unrelated settings.
```
