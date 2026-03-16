# 工作流示例：书籍章节开发

> 一个专注的单代理工作流，用于将原始素材转化为具有明确修订循环的战略第一人称章节草稿。

## 何时使用此工作流

当作者拥有语音笔记、片段或战略笔记，但还没有清晰的章节草稿时，使用此工作流。目标不是通用的代写。目标是生成能够加强类别定位、保留作者声音并清晰展示未决编辑决策的章节。

## 使用的代理

| 代理 | 角色 |
|------|------|
| Book Co-Author | 将素材转化为带编辑注释和后续问题的版本化章节草稿 |

## 示例激活

```text
Activate Book Co-Author.

Book goal: Build authority around practical AI adoption for Mittelstand companies.
Target audience: Owners and operational leaders of 20-200 person businesses.
Chapter topic: Why most AI projects fail before implementation starts.
Desired draft maturity: First substantial draft.

Raw material:
- Voice memo: "The real failure happens in expectation setting, not tooling."
- Notes: Leaders buy software before defining the operational bottleneck.
- Story fragment: We nearly rolled out the wrong automation in a cabinetmaking workflow because the actual problem was quoting delays, not production throughput.
- Positioning angle: Practical realism over hype.

Produce:
1. Chapter objective and strategic role in the book
2. Any clarification questions you need
3. Chapter 2 - Version 1 - ready for review
4. Editorial notes on assumptions and proof gaps
5. Specific next-step revision requests
```

## 预期输出结构

Book Co-Author 应回应五个部分：

1. `Target Outcome`
2. `Chapter Draft`
3. `Editorial Notes`
4. `Feedback Loop`
5. `Next Step`

## 质量标准

- 草稿保持第一人称视角
- 章节有清晰的承诺和内部逻辑
- 主张与素材相关联或标记为假设
- 删除通用的激励性语言
- 输出以明确的修订问题结束，而不是模糊的交接
