# EasyWrite

面向微信公众号与多场景表达的写作工具集。包含两个相互独立的工作模块：

- [Creation：观点池 → 选题角度 → 文章和标题封面](./creation/SKILL.md)
- [Rewrite：文章 → 多场景形式转写](./rewrite/README.md)
  - [TTS Renderer](./rewrite/renderers/tts/SKILL.md)
  - [Speech Renderer](./rewrite/renderers/speech/SKILL.md)

## 调用方式

**创作**：当作者已完成自由表达并发出明确指令后，读取 `creation/SKILL.md`；先扫描完整原始观点，借助不同创作方法探索候选角度并核验证据，由作者选定角度后，再根据要求组织文章、标题和封面。方法只是创作工具，不代表能够预测点击率。五种创作方法各自存放在 `creation/methods/`。

**转写**：提供已完成的原始母稿，指定 TTS 或 Speech Renderer，遵守 Rewrite 的 [Core 原则](./rewrite/core/principles.md)。不同 Renderer 直接读取原稿，互不依赖。创作和转写之间不存在自动执行或默认串联。

## 迁移来源

- 创作 Skill 来源：[Notion 原文档](https://app.notion.com/p/40b84e8891bf8101b462-e168347a867a)，[迁移快照](./creation/references/notion-original.md)。GitHub 是后续维护主源。
- Rewrite 模块源自 [orangeburn/SmartRewrite](https://github.com/orangeburn/SmartRewrite)，完整复制其 `main` 分支文件到 `rewrite/`；原仓库保持不变。
- 创作方法当前处于逐步设计阶段。已列出的点击机制是工作假设，不应宣称得到普遍因果证明。

## LICENSE

保留原仓库根目录 LICENSE；Rewrite 模块亦保留原项目 LICENSE。
