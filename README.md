# EasyWrite

**只记一个名字：`easywrite`，也可以说“用 ew”。** 创作、内容检查、口播和演讲转写集中在同一个 Skill，由它根据任务自行选择内部模块和方法。

## 使用

[SKILL.md](./SKILL.md) 是唯一入口。安装时将**仓库根目录**作为完整 Skill 文件夹，不单独安装内部模块。安装后的显式调用名称仍为 `$easywrite`；`ew` 是自然语言简称，不是另一个需要安装的 Skill。

```text
$easywrite 从下面这些观点里找切入角度
用 ew 跑一下这个大纲
用 ew 只检查标题能否准确表达正文
用 ew 按刚才确定的方向修改第二部分
用 ew 判断这篇完整文章能否发布
用 ew 把这篇文章转成可以直接念的播客稿
用 ew 把这篇文章转成上台演讲用的稿子
用 ew 对照原文检查这份口播稿有没有改变意思
```

在能访问本仓库的对话中也可提供仓库链接并说明任务；仓库可访问不等于客户端已安装，能否自动发现取决于客户端的 Skill 支持。

## 怎么选择工作流

EasyWrite 先确认**动作、材料阶段、处理范围和已确认事项**，再读取需要的规则。沿用当前对话已明确的角度、版本和约束，不反复从选题开始。

| 你要做什么 | 使用能力 | 交付边界 |
| --- | --- | --- |
| 从观点找切入角度 | [Creation](./creation/WORKFLOW.md) | 最多三个实质不同的候选，作者选定后才继续组织文章 |
| 写大纲、正文，修改局部或设计标题封面 | [Creation](./creation/WORKFLOW.md) | 从已有阶段继续，只完成请求的部分 |
| 检查大纲、片段、标题或某个维度 | [Review](./review/WORKFLOW.md) | 使用相关框架条目及必要关联检查，不给全篇发布结论 |
| 全文检查、完整发布审查 | [Review](./review/WORKFLOW.md) | 全文检查按材料阶段给意见；完整发布任务才给发布判断 |
| 需要措辞完整、可以直接朗读或合成语音的稿件 | [TTS](./rewrite/renderers/tts/WORKFLOW.md) | 从完整正式母稿生成口播稿 |
| 需要真人可自然换词的提词器稿或现场演讲稿 | [Speech](./rewrite/renderers/speech/WORKFLOW.md) | 按场景选择 Teleprompter 或 Stage |
| 检查、修订已有转写稿 | [Rewrite](./rewrite/README.md) | 对照母稿检查忠实度与场景适配，按授权范围修订 |

“用 ew 跑一下”接在大纲或稿件后，默认检查当前材料。观点仍在自由讨论时不自动选题；已有角度时不重新选题；检查不自动改稿；只改标题不自动生成封面；创作完成不自动进入审查或转写。

## 包含的能力

- **Creation**：从原始观点探索角度，按需组织逻辑、大纲、正文和标题封面。五种探索方法为情绪裁决、认知反转、异常解谜、利益揭示、荒诞现场，按任务选择，不强制遍历，不预测点击率。
- **Review**：使用[完整审查框架](./review/framework.md)，覆盖选题、受众、点击、第一屏、观点、增量、论证、传播、结构、表达、商业承接和发布 QA。区分专项检查与完整审查，只报告实质问题及最小修复；免费文章按实际阅读目标评审，不默认要求商业转化。
- **Rewrite**：通过 [Core](./rewrite/core/principles.md) 保留事实、观点、条件、判断力度和作者声音，再适配口播、提词器或现场演讲。各场景都直接回到原始母稿，不把另一种转写产物当母稿。这里交付文稿，实际语音和图片生成需要相应工具。

## 规则来源与维护

**本仓库是 EasyWrite 创作、审查和转写规则的唯一维护源。** Review 框架已从历史 Notion 文档迁入，后续直接维护 [review/framework.md](./review/framework.md)，不再从 Notion 同步或优先读取旧规则。Notion 仍可存放和提供文章、草稿、选题及观点，内容查询不受影响。

同一任务使用同一提交或已安装版本，已取得且未变化的规则和材料在上下文中复用；只加载当前任务需要的模块、方法及参考资料。

历史来源：

- Creation 源于 [Notion 原文](https://app.notion.com/p/40b84e8891bf8101b462e168347a867a)，保留[迁移快照](./creation/references/notion-original.md)供追溯。
- Review 源于 [Notion 历史框架](https://app.notion.com/p/3e784e8891bf809e879ec510d3d8c09d)，现以本仓库框架为准。
- Rewrite 源自 [orangeburn/SmartRewrite](https://github.com/orangeburn/SmartRewrite)，已整合为内部工作流；后续维护在本仓库完成。

## LICENSE

保留根目录 LICENSE 与 Rewrite 模块 LICENSE。
