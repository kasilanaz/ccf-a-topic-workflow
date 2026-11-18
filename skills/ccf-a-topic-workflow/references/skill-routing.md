# 可选模块与分工

主流程可以独立使用。当前会话已提供下列 skill 时，将对应环节交给它，统一保留种子论文、证据位置和引用链接。未提供该模块时，用当前会话的论文读取与检索能力执行本工作流的同一环节。检索不可用时，在提供的材料范围内分析，将外部查新标为待核实。

| 环节 | 可选模块 | 传给模块的任务 |
| --- | --- | --- |
| 方向、局限与候选题 | [Claude Scholar · research-ideation（Codex）](https://github.com/Galaxy-Dawn/claude-scholar/blob/codex/skills/research-ideation/SKILL.md) | 从指定论文提取方法、条件、局限和证据，形成问题卡。论文规模较大或结论难以比较时，可用 [Supervisor · deep-research](https://github.com/HKUSTDial/Supervisor-Skills/blob/main/skills/deep-research/SKILL.md) 协助做跨论文综合。 |
| 候选查新 | [ARIS · novelty-check](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/novelty-check/SKILL.md) | 输入候选问题、各条拟贡献和现有证据，逐项返回近邻论文、重叠范围和实质差异。为会左右判定的主张复核全文。 |
| 概念评审 | [CCFA · ccf-idea-reviewer](https://github.com/mikubaka88/CCFA-Skills/blob/main/ccf-idea-reviewer/SKILL.md) | 输入问题、文献来源、近邻、查新表及目标方向的正式论文，按概念评审范围检查问题价值、洞察和相对贡献，给出最强质疑及证据。汇总时仍须检查本工作流的四项准入条件。 |

只调用相关模块。完整调研、外部评审、实验或写作流程按实际任务和授权另行选择。汇总时以可追溯的论文证据作为最终判断依据。
