<h1 align="center">MotionSites Web Builder 中文版（motionsites-zh）</h1>

<p align="center"><b>让 Claude 产出获奖级、电影感的落地页，而不是平庸的 AI 布局。</b></p>

<p align="center">
  <a href="https://github.com/Motionsites-AI/claude-skill">上游 Motionsites-AI/claude-skill</a> ·
  <a href="https://motionsites.ai">MotionSites 官网</a>
</p>

> **这是什么**：本仓库是 [Motionsites-AI/claude-skill](https://github.com/Motionsites-AI/claude-skill) 的非官方简体中文汉化版，仅包含上游 **MIT 许可的部分**（技能指令、参考文档与脚本）。汉化说明 by [@bayshier](https://github.com/bayshier)。
>
> **关于 examples 与 media**：上游的 `examples/`（40 个示例提示词）与 `media/`（媒体架）为 MotionSites 专有（© MotionSites，允许用于建站但禁止作为提示词/媒体集合再分发），**因许可限制不在本仓库**。请到[上游仓库](https://github.com/Motionsites-AI/claude-skill)获取完整技能，或直接用上游的插件市场命令安装。
>
> **翻译范围**：README 为中文；`SKILL.md`、`references/`、`scripts/` 是 Agent 运行时消费层，**逐字节保留英文**以保证行为与上游一致。

## 它解决什么

AI 建的网站千篇一律，原因有三：规划含糊、没有真实媒体、没人看结果。这个技能把三个都修了——Claude 会研读 [MotionSites](https://motionsites.ai) 上最受欢迎的设计，挑选真实的电影级素材，写一份精确的构建规范，构建页面，然后**截自己作品的屏幕并不断修改**，直到达到图库级标准。

技能内含 **40 个示例设计**，每个都展示在它所基于的 hero 视频旁。全部 50+ 视频都在技能的媒体架上。

## 里面有什么

- **40 个示例提示词**：MotionSites 上最受欢迎的免费提示词，是人们真正喜欢的那些设计。Claude 会对每个需求精读最接近的 2–3 个，以匹配它们的细节密度与品味。
- **媒体架**：50+ 电影级 hero 视频、30 个透明 3D 抠图与 29 张图片，公开托管，以编号联系表呈现——Claude 用眼睛挑选素材。
- **55+ 技巧配方**（附可运行代码），例如：无缝视频循环、液态玻璃、逐词模糊标题、鼠标搓擦视频、聚光揭示、纵深轮播、滚动叙事、真 3D 模型（Three.js）。
- **带真实数字的品味规则**：字号阶梯、字距、间距、颜色、动效时序与文案。
- **规格模板**：Claude 写代码前先写精确构建规范——质量就是在这一步决定的。
- **查看-修改循环**：截图 + QA 脚本（坏资源、移动端溢出、字体、视频播放）+ 一份评分标准。
- **提示词模式**：只要提示词不要代码时，产出为 Lovable、Bolt、v0、Cursor、Manus、Google AI Studio 或 Kimi 调校过的提示词。

## 安装

### Claude.ai 与 Claude 桌面端
1. 从[最新 release](https://github.com/Motionsites-AI/claude-skill/releases/latest) 下载 **`motionsites-web-builder.zip`**。
2. 在 Claude 里打开 **Customize → Skills → + → Create skill → Upload a skill**，选择 zip 并开启技能（需在 Settings → Capabilities 里启用代码执行）。

### Claude Code（插件）
```
/plugin marketplace add Motionsites-AI/claude-skill
/plugin install motionsites-web-builder@motionsites
```
没有 GitHub SSH key？改用 `/plugin marketplace add https://github.com/Motionsites-AI/claude-skill.git`。

### Claude Code（手动）
把 `plugins/motionsites-web-builder/skills/motionsites-web-builder` 拷贝到 `~/.claude/skills/`。

### 可选：让 Claude 看见自己的作品
查看-修改循环配 Playwright 效果最好：
```
pip install playwright && python -m playwright install chromium
```

## 试试看

直接向 Claude 要一个网站，技能会自动触发：

- *「为一个奢华睡眠监测戒指做一个落地页 hero。」*
- *「给一位里斯本的建筑摄影师做个作品集主页。编辑风、安静。」*
- *「为我的 AI 旅行应用写一个 Lovable 等待页提示词。」*
- *「这是我现在的主页：把它做得像获奖作品。」*

## 想要完整库？

本技能里的示例与媒体是**免费样品**。[MotionSites Unlimited](https://motionsites.ai/unlimited) 解锁：500+ 高级网站提示词（适配 Lovable、Bolt、v0、Cursor 与 Claude）、动效 hero 背景与分区提示词、40+ Lovable 模板、MotionSites MCP（Claude 可直接检索并拉取任意高级提示词进构建）、个人与客户项目均可使用。

## 许可证

见 [LICENSE](LICENSE)。技能的指令与代码为 **MIT**（© 2026 MotionSites）——本仓库仅包含并汉化这一部分。示例提示词与媒体仍为 © MotionSites：可在用本技能构建的网站中使用，但不得转售或作为提示词/媒体集合再分发（因此不在本仓库）。中文 README 由 [@bayshier](https://github.com/bayshier) 添加，与上游及 OpenAI/Anthropic 无隶属关系。
