# MyHtml Editor

一款轻量级、本地化的 HTML 可视化编辑器，专为快速编辑演示文稿、简历、信息图表等单页/多页 HTML 文件而设计。

## 项目背景

MyHtml 是基于开源项目 [htmltool2](https://github.com/caoxianqi/htmltool2)（作者 [caoxianqi](https://github.com/caoxianqi)）进行的二次开发，整个开发过程由 AI 辅助完成。原项目提供了核心的 iframe 预览、文本编辑和颜色面板功能，MyHtml 在此基础上新增了撤销/重做、图片插入与操作、页面滚动导航、智能调色板切换等特性。

## 功能特性

### 核心编辑
- **单文件应用**：打开 `MyHtml.html` 即可使用，无需安装
- **完全本地化**：所有操作在浏览器中完成，文件不上传
- **脚本模式默认开启**：打开 HTML 自动启用 JavaScript，支持动画和交互页面
- **文本编辑**：开启编辑模式后点击文字直接修改，粘贴自动转纯文本
- **颜色编辑**：点击元素空白处弹出颜色面板，支持背景色、文字色、HEX 输入和快捷调色板
- **快捷调色板智能切换**：最后聚焦背景色输入框则应用到背景，聚焦文字色则应用到文字

### 撤销 / 重做
- `Ctrl+Z` 撤销，`Ctrl+Shift+Z` 或 `Ctrl+Y` 重做
- 最多保存 50 步历史记录
- 编辑文字和修改颜色均支持撤销重做
- 撤销时保持编辑模式和滚动位置不丢失

### 页面滚动
- **滚轮翻页**：鼠标在任意位置滚动滚轮即可翻页
- **键盘方向键**：`↑` `↓` `←` `→` 滚动页面
- **Page Up / Page Down**：快速翻页
- **Ctrl+Home / Ctrl+End**：跳转到顶部 / 底部
- 编辑模式下方向键自动区分：光标在文字中移动光标，在空白处滚动页面

### 插入图片
- 点击工具栏图片按钮选择本地图片插入
- 图片自动转为 data URL 内嵌
- **自由拖拽移动**：按住图片拖拽调整位置
- **四角缩放**：拖拽四角手柄调整大小
- **自动锁定页面**：图片插入到当前激活的幻灯片内部，切换页面时自动隐藏，切回时自动显示
- 选中图片后按 `Delete` 或 `Backspace` 删除
- 按 `Esc` 取消选中

### 文件操作
- 拖放 `.html` / `.htm` 文件到窗口打开
- 保存时自动内联图片为 data URL
- 实时显示文件修改状态

## 快速开始

在浏览器中打开：

```
MyHtml.html
```

点击「打开」按钮或拖拽 HTML 文件到窗口。

如果 HTML 依赖相对路径资源，启动本地服务器：

```bash
python -m http.server 8765
```

然后访问 `http://127.0.0.1:8765/MyHtml.html`

## 快捷键

| 快捷键 | 功能 |
| --- | --- |
| `Ctrl` + `S` | 保存 |
| `Ctrl` + `Z` | 撤销 |
| `Ctrl` + `Shift+Z` / `Ctrl+Y` | 重做 |
| `↑` `↓` `←` `→` | 滚动页面 |
| `Page Up` / `Page Down` | 快速翻页 |
| `Ctrl` + `Home` / `End` | 跳转顶部 / 底部 |
| `Delete` / `Backspace` | 删除选中图片 |
| `Esc` | 关闭面板 / 取消选中 |

## 与 htmltool2 的关系

MyHtml 的核心编辑架构（iframe 预览、contentEditable 文本编辑、颜色面板、overlay 高亮系统）源自 [htmltool2](https://github.com/caoxianqi/htmltool2)。在此基础上，MyHtml 由 AI 辅助开发，新增了以下功能：

- 撤销 / 重做（50 步历史）
- 图片插入、拖拽移动、四角缩放、删除
- 滚轮翻页、键盘方向键导航、Page Up/Down
- 快捷调色板智能切换
- 幻灯片感知（自动检测当前激活页面）
- 深色主题 UI

## 项目结构

```
MYhtml/
├── MyHtml.html             # 编辑器主文件
├── test.html               # 示例测试页面
├── README.md               # 中文文档
├── README_EN.md            # 英文文档
├── LICENSE                 # MIT License (Copyright (c) 2026 Bin)
└── THIRD_PARTY_NOTICES.md  # 第三方项目声明
```

## 浏览器兼容性

推荐最新版 Chrome 或 Edge。Safari 和 Firefox 可用，但编辑行为可能有差异。

## 致谢

- [htmltool2](https://github.com/caoxianqi/htmltool2) by [caoxianqi](https://github.com/caoxianqi) — MyHtml 的基础架构来源，MIT License
- AI 辅助开发 — 代码编写与功能扩展由 AI 协助完成

## 许可证

MIT License — 详见 [LICENSE](LICENSE)

第三方项目声明详见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
