# EasyWrite

**只记一个名字：`easywrite`。** 创作、文章审查、口播/演讲转写集中在同一个 Skill 下；不会因为调用 EasyWrite 而自动执行所有阶段。

## 唯一入口

[**SKILL.md**](./SKILL.md) — `name: easywrite`。安装时将**仓库根目录**作为一个完整 Skill 文件夹，而不是单独安装 `creation/` 或两个 Renderer。安装后使用 `$easywrite`，再用自然语言说明任务，例如：

```text
$easywrite 从下面这些观点里找切入角度
$easywrite 审查《文章标题》是否适合发布
$easywrite 把下面的文章转成播客口播稿
```

在可访问此仓库的 ChatGPT 对话中，也可以直接说“用 easywrite 审查这篇文章”；是否自动识别为安装 Skill 取决于客户端是否已连接/安装，**仓库本身不等于已安装**。

## 内部模块

- [Creation](./creation/WORKFLOW.md)：观点池 → 不同叙事角度 → 作者选定后组织文章、标题与封面。五种探索方法和 References 按需加载，不声称能预测点击率。
- [Review](./review/WORKFLOW.md)：按 [微信公众号商业写作发布前审查框架（Notion 完整快照）](./review/framework.md) 审查传播、观点、商业价值和发布风险。12 项内部检查，输出只保留实际问题；Notion 在线可用时优先读取最新原文。
- [Rewrite](./rewrite/README.md)：从完整正式原稿出发，经 [Core](./rewrite/core/principles.md) 分别生成 [TTS 口播稿](./rewrite/renderers/tts/WORKFLOW.md) 或 [Speech 演讲稿](./rewrite/renderers/speech/WORKFLOW.md)。

## 来源与版本

- Creation 源于 [Notion 原文](https://app.notion.com/p/40b84e8891bf8101b462e168347a867a)，[历史快照](./creation/references/notion-original.md)。当前维护以 GitHub 为准。
- Review 主框架源于 [Notion「草稿」数据库](https://app.notion.com/p/3e784e8891bf809e879ec510d3d8c09d)，仓库保留完整正文快照；在线审查优先以现行 Notion 版为准。
- Rewrite 源自 [orangeburn/SmartRewrite](https://github.com/orangeburn/SmartRewrite)。为实现单 Skill 安装，内层 Skill 清单改为 `WORKFLOW.md`，工作流规则和素材内容保留，原独立仓库未修改。
- 非用户明确要求时，不默认依次运行 Creation → Review → Rewrite；DBS 仅在明确请求或专项规则要求时通过其线上主路由真实执行。

## LICENSE

保留根目录 LICENSE 与 Rewrite 模块 LICENSE。
