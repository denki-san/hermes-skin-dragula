[English](README.md) | **中文**

# 🧛 Hermes Skin: Dracula

为 [Hermes Agent](https://github.com/NousResearch/hermes-agent) 打造的 [Dracula](https://draculatheme.com) 暗色主题皮肤。

## 预览

| 默认皮肤 | Dracula 皮肤 |
|:---:|:---:|
| ![Default](assets/default-skin.png) | ![Dracula](assets/dracula-skin.png) |

### 特性

- 🎨 基于 Dracula 官方色板（Purple / Pink / Cyan / Green / Comment）
- ✟ 统一 Unicode 哥特风符号
- ⚰ 吸血鬼主题 branding（The Count Decrees / Until the next moonrise...）
- 🦇 自定义 ASCII banner 和像素 hero art

## 安装

**1. 复制皮肤文件到 Hermes skins 目录：**

```bash
cp dracula.yaml ~/.hermes/skins/
```

**2. 在 Hermes 中切换皮肤：**

```
/skin dracula
```

**3.（可选）设为默认皮肤：**

编辑 `~/.hermes/config.yaml`：

```yaml
display:
  skin: dracula
```

## 💡 Tips

- **搭配 Dracula 人格效果更佳！** 在 `~/.hermes/personalities/` 下创建一个 `dracula.yaml`，让你的 Agent 以德古拉伯爵的口吻回答问题——古典、优雅、略带傲慢。
- **终端配色建议**：搭配 [Dracula for iTerm](https://draculatheme.com/iterm) 或 [Dracula for Terminal.app](https://draculatheme.com/terminal-app) 使用，背景色一致效果最佳。
- **自定义 tool_emojis**：`tool_emojis` 的 key 取决于你加载的工具名称，可以在 Hermes 启动后看 Available Tools 列表，按实际工具名配置。

## 致谢

- **文档参考**：[Hermes Skins 官方文档](https://hermes-agent.nousresearch.com/docs/zh-Hans/user-guide/features/skins)
- **配色参考**：[Dracula Theme](https://github.com/dracula/dracula-theme)
- **ASCII Art 参考**：[asciiart.website](https://asciiart.website/index.php)
- **灵感启发**：[joeynyc/hermes-skins](https://github.com/joeynyc/hermes-skins)

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
