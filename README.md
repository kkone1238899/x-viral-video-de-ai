# 去 AI 味

> 内容一眼 AI 味没人信？这个库收集去 AI 味、人性化改写的工具，每条都写清楚能帮你解决什么、怎么用它搞钱。
>
> A curated collection of de-AI-ing & humanizing AI content prompts & skills for viral short videos, gathered from practitioners sharing on X.
> 
> Each entry answers two questions: what problem it solves (and who it's for), and how to make money with it.
> 
> Star counts verified via GitHub API on 2026-10-12. Continuously updated.

## 条目

### iniwap/AIWriteX

**核心提炼**
- 解决什么问题：AI 写的中文内容一眼被识破，公众号爆文从选题到发布链路又长又散。它把热点选题 → 洗稿/原创 → 去 AI 味润色 → 自动配图 → 多平台发布做成一条线，还自带 AI 检测对抗引擎（结构粉碎、动态风格拟态）。
- 核心用法（5 步）：1) 输入热点选题、已有文章或对标公众号；2) 在"文案武库"选场景（短视频口播、影视解说等 24 个）；3) 选模式生成：原创 / 仿写 / 转换；4) 过"去 AI 味"对抗引擎，打散 AI 的结构指纹；5) 输出逐句换行的口播稿或排版好的图文，直接发布或拿去配音。
- 什么时候用 / 常见坑：需要量产中文口播稿/图文时用。作者自己提醒：朱雀这类检测器持续进化，纯 AI 长文越来越难过检测，建议人机混合（AI 出初稿、人大幅改），别指望一遍过。

**适用场景**：中文自媒体内容团队、做账号代运营的人。

**怎么用它搞钱**：自媒体洗稿 / 代写 / 账号代运营——按账号收代运营费，或按篇收爆文代写费。

**来源**：[iniwap/AIWriteX](https://github.com/iniwap/AIWriteX) · ⭐2069 · 更新于 2026-10-12

### rudra496/StealthHumanizer

**核心提炼**
- 解决什么问题：英文（及多语言）AI 文案被 GPTZero、Turnitin 这类检测器抓，又不想为付费 humanizer 花钱、也不想注册账号。
- 核心用法（4 步）：1) 输入：把 AI 生成的文本粘贴到网页版或 CLI；2) 选改写强度：Light / Medium / Aggressive / Ninja 四档；3) 选文风与用途：6 种文风、9 种用途、13 种语气；4) 输出：本地检测评分 + 改写结果，可导出 TXT/DOCX/PDF，不满意点 Refine 再压一轮。
- 什么时候用 / 常见坑：短文本（≤150 词）走默认模型几秒出结果；长文自动走 gemma3:4b，需要 25–90 秒，别误以为卡死。支持 16+ 语言，含简繁中文。

**适用场景**：做英文内容出海、跨境电商 listing、英文博客的内容团队。

**怎么用它搞钱**：内容团队润色服务——接海外内容团队、跨境卖家的英文 listing/博客润色单，按量收费。

**来源**：[rudra496/StealthHumanizer](https://github.com/rudra496/StealthHumanizer) · ⭐167 · 更新于 2026-10-09

### lynote-ai/humanize-text

**核心提炼**
- 解决什么问题：市面上的 humanizer 都是黑盒、营销话术多。这个项目开源了整套"去 AI 味"管线：教模型改写文本结构，而不只是表面换同义词，方法可审计。
- 核心用法（4 步）：1) 输入：草稿存成 draft.txt；2) 配 key：复制 config.example.toml，填 DeepSeek/OpenRouter 的 API key；3) 跑管线：`python -m src.standard.pipeline --input draft.txt`；4) 输出：多轮改写后的自然文本；想自己训练模型可看 training-data-pipeline/ 里的 SFT+KTO 数据构造文档。
- 什么时候用 / 常见坑：想自己搭一条可审计的去 AI 味管线、或研究"结构改写"方法论时用。项目不发货成品权重和效果承诺，需要你有 LLM key 和跑 Python 的环境。

**适用场景**：有技术能力、想把去 AI 味做成自己生产管线一环的内容团队或独立开发者。

**怎么用它搞钱**：把这条"结构改写"管线封装成自己的内容生产工具，对外提供 AI 内容人性化代处理服务；方法论全部公开，也可做成课程或咨询。

**来源**：[lynote-ai/humanize-text](https://github.com/lynote-ai/humanize-text) · ⭐3350 · 更新于 2026-10-08

### Wechat-ggGitHub/chinese-ai-humanizer

**核心提炼**
- 解决什么问题：中文口播稿/文案里的 AI 腔（连接词堆砌、"不是……而是……"翻案句这类稳定特征）。规则清单极简，给 Agent 用，token 成本低。
- 核心用法（3 步）：1) 安装：`git clone` 到 `~/.agents/skills/chinese-ai-humanizer`（Codex/Claude Code），或把 SKILL.md 正文粘进 AGENTS.md / CLAUDE.md；2) 调用：直接说"帮我去除下面这段文字的 AI 味"，或显式 `$chinese-ai-humanizer`；3) 输出：Agent 按规则清单改写后的自然中文。
- 什么时候用 / 常见坑：写中文口播稿、公众号文案时常驻开启。作者明确边界：只减少常见中文 AI 腔，不提供检测功能、不保证绕过检测工具。

**适用场景**：中文内容创作者；想在 Agent 写稿流程里加一道"去味"工序的人。

**怎么用它搞钱**：中文短视频口播代写 / 润色服务——把这个 skill 接进自己的 Agent 写稿管线，按条或按账号收润色费；"稿子不像 AI 写的"本身就是代运营的差异化卖点。

**来源**：[Wechat-ggGitHub/chinese-ai-humanizer](https://github.com/Wechat-ggGitHub/chinese-ai-humanizer) · ⭐82 · 更新于 2026-08-23

### ilien-dev/quiron

**核心提炼**
- 解决什么问题：Agent 改写完，不知道到底去没去干净。它给模型一份 33 条 AI 写作特征清单，改完再用测量器对照人类写作基准打分——有没有效用数字说话，不是凭感觉。
- 核心用法（3 步）：1) 安装：`npx skills add ilien-dev/quiron`（Claude Code / Codex / Cursor，无需 API key）；2) 调用：把草稿丢给 Agent 让它 humanize；3) 输出：改写后的文本 + 测量结果（多少项特征落在人类区间），没达标继续压。
- 什么时候用 / 常见坑：适合润色自己或团队内部的文案（作者声明不建议用来冒充人类公开发布）。纯 Python 标准库、无外部依赖。

**适用场景**：用 Agent 写英文博客、教程、文档的内容创作者。

**怎么用它搞钱**：给英文内容团队做"去 AI 味质检"——按篇提供"改写 + 人类度评分报告"，比单纯改写多一层可交付的证据；也可打包进英文内容代写服务里提价。

**来源**：[ilien-dev/quiron](https://github.com/ilien-dev/quiron) · ⭐57 · 更新于 2026-09-25

## 收录标准

- 来源：X 博主实战分享（原帖 / 评论区 / 引用链）及 GitHub 高星项目
- 每条格式：核心提炼（解决什么问题 / 核心用法 / 什么时候用与常见坑）+ 适用场景 + 一条「怎么用它搞钱」+ 来源（链接只作来源，star 数与更新时间以 GitHub API 为准）
- 用户视角写作：不写满，禁用"全网最全／唯一／第一／没人做"等断言；没读到的不写
- 去重：同一项目只收录一次，不堆 raw 链接

## 相关分类

- 总索引：[x-viral-video-skills](https://github.com/kkone1238899/x-viral-video-skills) —— 13 个分类导航
- [x-viral-video-scripts](https://github.com/kkone1238899/x-viral-video-scripts) —— 编剧 / 脚本
- [x-viral-video-hooks](https://github.com/kkone1238899/x-viral-video-hooks) —— 标题 / 5 秒钩子
- [x-viral-video-creative-direction](https://github.com/kkone1238899/x-viral-video-creative-direction) —— 创意总监
- [x-viral-video-directing](https://github.com/kkone1238899/x-viral-video-directing) —— 导演
- [x-viral-video-replication](https://github.com/kkone1238899/x-viral-video-replication) —— 复制爆款
- [x-viral-video-breakdown](https://github.com/kkone1238899/x-viral-video-breakdown) —— 拉片
- [x-viral-video-pipeline](https://github.com/kkone1238899/x-viral-video-pipeline) —— 流水线 / 生产管线
- [x-viral-video-characters](https://github.com/kkone1238899/x-viral-video-characters) —— 人物构建
- [x-viral-video-editing](https://github.com/kkone1238899/x-viral-video-editing) —— 视听剪辑技巧
- [x-viral-video-prompt-opt](https://github.com/kkone1238899/x-viral-video-prompt-opt) —— 提示词优化
- [x-viral-video-copywriting](https://github.com/kkone1238899/x-viral-video-copywriting) —— 文案
- [x-viral-video-showcase](https://github.com/kkone1238899/x-viral-video-showcase) —— X 病毒视频合集

## 投稿

发现好的去 AI 味 prompt / skill，欢迎提 Issue 或 PR（格式见 CONTRIBUTING.md）。

## 更新日志

- 2026-10-12：条目升级为小节格式（核心提炼 / 适用场景 / 怎么用它搞钱 / 来源）；新增 3 个项目（lynote-ai/humanize-text、Wechat-ggGitHub/chinese-ai-humanizer、ilien-dev/quiron）
- 2026-10-11：首版，2 个项目，持续收录中
