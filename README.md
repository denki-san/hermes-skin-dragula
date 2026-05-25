**English** | [中文](README.zh-CN.md)

# 🧛 Hermes Skin: Dracula

A [Dracula](https://draculatheme.com) dark theme skin for [Hermes Agent](https://github.com/NousResearch/hermes-agent).

## Preview

| Default Skin | Dracula Skin |
|:---:|:---:|
| ![Default](assets/default-skin.png) | ![Dracula](assets/dracula-skin.png) |

### Features

- 🎨 Built on the official Dracula palette (Purple / Pink / Cyan / Green / Comment)
- ✟ Consistent Unicode gothic glyphs
- ⚰ Vampire-themed branding (*The Count Decrees* / *Until the next moonrise...*)
- 🦇 Custom ASCII banner and pixel hero art

## Installation

**1. Copy the skin file into the Hermes skins directory:**

```bash
cp dracula.yaml ~/.hermes/skins/
```

**2. Switch to the skin inside Hermes:**

```
/skin dracula
```

**3. (Optional) Set it as the default skin:**

Edit `~/.hermes/config.yaml`:

```yaml
display:
  skin: dracula
```

## 💡 Tips

- **Pair it with a Dracula personality for the best effect.** Create a `dracula.yaml` under `~/.hermes/personalities/` so your Agent answers in the voice of Count Dracula — classical, elegant, and a touch haughty.
- **Terminal color suggestion**: combine with [Dracula for iTerm](https://draculatheme.com/iterm) or [Dracula for Terminal.app](https://draculatheme.com/terminal-app); a matching background looks best.
- **Customize `tool_emojis`**: the `tool_emojis` keys depend on the tool names you load. Check the Available Tools list once Hermes is up and configure them to match the actual names.

## Credits

- **Docs reference**: [Hermes Skins official docs](https://hermes-agent.nousresearch.com/docs/zh-Hans/user-guide/features/skins)
- **Palette reference**: [Dracula Theme](https://github.com/dracula/dracula-theme)
- **ASCII art reference**: [asciiart.website](https://asciiart.website/index.php)
- **Inspiration**: [joeynyc/hermes-skins](https://github.com/joeynyc/hermes-skins)

## License

MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
