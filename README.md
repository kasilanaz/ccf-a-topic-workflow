# CCF-A 科研选题工作流

这是一个从已有论文出发筛选 CCF-A 主选题的 Agent Skill。它根据你提供的 PDF、DOI 或论文链接，梳理研究方向、已有工作和不足，查新并逐条核对拟创新点，再对照同方向的 CCF-A 正式论文判断贡献。

## 在 Codex 中使用

克隆或下载这个仓库，在 Codex 中打开仓库目录。把论文 PDF 放在当前项目中，或在聊天里提供 DOI 和论文链接，然后发送：

```text
请读取 skills/ccf-a-topic-workflow/SKILL.md，按这套工作流分析我提供的论文。
先梳理各研究方向、代表工作和有证据的不足。基于这些证据提出候选研究问题，
再追踪后续工作，逐条核查拟创新点并对标同方向的 CCF-A 正式论文。
只给出通过准入审查的主选题，附研究问题、拟创新点、近邻差异和推荐理由。
证据不足的单列预研。如果没有达标题，请报告本轮无主选题，并说明原因。
```

将 [`skills/ccf-a-topic-workflow`](skills/ccf-a-topic-workflow) 整个目录加入当前项目的 `.agents/skills/` 后，也可以通过 `$ccf-a-topic-workflow` 调用。

## 会得到什么

1. **研究方向图**：各条路线解决的问题、代表文献、进展和待回答的问题。
2. **文献证据表**：已有贡献、成立条件、局限的类型、原文位置及后续覆盖情况。
3. **查新与创新点核查**：最接近的工作、已覆盖范围、剩余差异、检索词和查新日期。
4. **CCF-A 准入表**：逐项审核问题证据、创新增量、发表案例对标和最强审稿质疑。
5. **主选题卡**：题目、要解决的问题、生成原因、拟创新点及证据链接。根据准入结果给出推荐，通常为 1–3 题，也可以是零题。预研与淘汰项单列。

查新覆盖密切相关的会议、期刊和预印本。CCF-A 正式论文用于比较贡献尺度和目标方向的匹配度。交付范围是研究问题与拟贡献核查。

主流程可独立使用。如果当前环境已配好 Claude Scholar、ARIS、CCFA-Skills 或 Supervisor-Skills，可以按 [模块分工](skills/ccf-a-topic-workflow/references/skill-routing.md) 使用其中的相关模块。

[工作流入口](skills/ccf-a-topic-workflow/SKILL.md) · [证据与查新规则](skills/ccf-a-topic-workflow/references/evidence-and-review.md) · [CCF-A 准入规则](skills/ccf-a-topic-workflow/references/ccf-a-admission.md) · [输出模板](skills/ccf-a-topic-workflow/references/output-templates.md)
