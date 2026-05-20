# Hermes Skin 配色指南

> 基于 Hermes Agent v0.14.0 的 skin 配置经验总结，方便制作新主题时参考。

## 色值配置项总览

### Colors 配置项与 UI 对应关系

| 配置项 | 控制的 UI 元素 | 视觉位置 |
|--------|--------------|---------|
| `banner_border` | 启动 banner 面板的边框线 | 启动界面外框 |
| `banner_title` | banner 标题文字（如 "Hermes Agent v0.14.0..."） | 启动界面顶部 |
| `banner_accent` | banner 中的章节标题（"Available Tools"、"Available Skills"） | 启动界面内容区 |
| `banner_dim` | banner 中的次要文本（分隔符、次要标签、如 "(and 22 more toolsets...)"） | 启动界面弱化文字 |
| `banner_text` | banner 正文（工具名、技能名列表） | 启动界面列表文字 |
| `ui_accent` | 通用 UI 强调色（输入框上下的横线等） | 输入区分隔线 |
| `ui_label` | UI 标签和标记 | 分类标签 |
| `ui_ok` | 成功指示器（✓） | 成功提示 |
| `ui_error` | 错误指示器 | 错误提示 |
| `ui_warn` | 警告指示器 | 警告提示 |
| `prompt` | 用户输入文字的颜色 | 输入光标处 |
| `input_rule` | 输入区域上方的横线 | 输入框装饰线 |
| `response_border` | AI 回复区块的边框线（含 response_label 那行） | 回复区边框 |
| `session_label` | Session 标签颜色 | 左侧面板 |
| `session_border` | Session 边框暗色 | 左侧面板边框 |
| `status_bar_bg` | 状态栏整条背景色 | 底部状态栏 |
| `status_bar_text` | 状态栏普通文字（token 数、时间等） | 底部状态栏 |
| `status_bar_strong` | 状态栏强调文字（模型名、⚕ 符号） | 底部状态栏 |
| `status_bar_dim` | 状态栏弱化元素（│ 分隔符、进度条空槽） | 底部状态栏 |
| `status_bar_good` | 状态栏正常状态（进度条已填充部分） | 底部状态栏 |
| `status_bar_warn` | 状态栏警告状态 | 底部状态栏 |
| `status_bar_bad` | 状态栏错误状态 | 底部状态栏 |
| `status_bar_critical` | 状态栏严重错误 | 底部状态栏 |
| `voice_status_bg` | 语音模式状态背景 | 语音模式 |
| `completion_menu_bg` | 补全菜单背景 | Tab 补全 |
| `completion_menu_current_bg` | 补全菜单当前选中行背景 | Tab 补全 |
| `completion_menu_meta_bg` | 补全菜单 meta 列背景 | Tab 补全 |
| `completion_menu_meta_current_bg` | 补全菜单 meta 列选中行背景 | Tab 补全 |

## 默认 Skin 的色值共享关系（一致性规则）

Hermes 默认 skin 中，以下配置项设计为**共用同一色值**，代表它们属于同一视觉角色：

| 逻辑角色 | 共享的配置项 | 默认 skin 色值 |
|---------|------------|--------------|
| **边框色** | `banner_border` = `input_rule` | `#CD7F32` |
| **标题/强调色** | `banner_title` = `response_border` | `#FFD700` |
| **高亮色** | `banner_accent` = `ui_accent` | `#FFBF00` |
| **正文色** | `banner_text` = `prompt` | `#FFF8DC` |
| **深色背景** | `status_bar_bg` = `voice_status_bg` = `completion_menu_bg` = `completion_menu_meta_bg` | `#1a1a2e` |
| **选中背景** | `completion_menu_current_bg` = `completion_menu_meta_current_bg` | `#333355` |

> **制作新主题时，应确保同一逻辑角色内的配置项使用相同色值。**
> 除非有意打破一致性（如让 response_border 比 banner_title 更低调）。

## 不受 Skin 控制的元素（硬编码）

以下 UI 元素的颜色由 Hermes 源码硬编码，yaml 配置**无法覆盖**：

- Available Tools 列表中特殊工具的高亮色（如黄色的 `browser_cdp`、`computer_use`、`discord`）
- Status bar 前面的 `⚕` 符号本身（符号不可改，颜色由 `status_bar_strong` 控制）
- `prompt_symbol`（符号文字由 `branding.prompt_symbol` 控制，但默认的 `⚕` 来自源码）

## Status Bar 结构说明

Status bar 分为两行，从上到下：

```
⚕ claude-opus-4-7 │ 27.2K/262.1K │ [█░░░░░░░░░] 10% │ 2m │ ⏱ 44s
────────────────────────────────────────────────────────────────────
⚕ 🕯️ msg=interrupt · /queue · /bg · /steer · Ctrl+C cancel
```

| 元素 | 控制它的配置项 |
|------|-------------|
| `⚕` + 模型名 | `status_bar_strong` |
| 数值文本（token、时间） | `status_bar_text` |
| `│` 分隔符、进度条空槽 `░` | `status_bar_dim` |
| 进度条填充 `█` | `status_bar_good` |
| 两行之间的横线 | `ui_accent` |
| 底部提示行文字 | `banner_dim` |
| 整体底色 | `status_bar_bg` |

## 新主题配色步骤建议

1. **确定主色调**：选 3-5 个主题色（如 Dracula 用 Purple/Cyan/Pink/Green/Comment）
2. **分配逻辑角色**：
   - 边框色 → 选一个中性/暗淡的颜色
   - 标题/强调色 → 选一个醒目但不过度的颜色
   - 高亮色 → 选主题里最标志性的强调色
   - 正文色 → 前景白/浅色
   - 深色背景 → 比终端背景略深或略浅
3. **按一致性规则赋值**：同一逻辑角色的配置项用相同色值
4. **单独调优**：status_bar 系列可以按需微调层次
5. **验证**：重新加载 skin 后检查各区域色彩是否协调

## Dracula 主题的配色映射参考

| Dracula 色板 | 色值 | 适合的逻辑角色 |
|-------------|------|--------------|
| Background | `#282a36` | 深色背景（status_bar_bg 等） |
| Current Line | `#44475a` | 选中背景（completion_menu_current_bg） |
| Foreground | `#f8f8f2` | 正文色（banner_text、prompt） |
| Comment | `#6272a4` | 边框色 / dim 元素 |
| Cyan | `#8be9fd` | 标签、session_label |
| Green | `#50fa7b` | 成功色、ui_ok |
| Orange | `#ffb86c` | 警告色、ui_warn |
| Pink | `#ff79c6` | 标题色、response_border |
| Purple | `#bd93f9` | 高亮色（banner_accent、ui_accent） |
| Red | `#ff5555` | 错误色 |
| Yellow | `#f1fa8c` | 备选警告色 |
