# Evolution-Agent

一套面向专业开发、开盒即用的通用 AGENT 框架。它为 Codex 提供项目规则、可独立选用的技能，以及从理解需求到交付、留痕和迭代的工作方式。

| 特色 | 框架怎样实现 |
|---|---|
| 高效交流 | 先简述核心效果，探查后把依据、做法和交付结果汇报给用户。追加需求并入同一份制作表，AI 按已有授权持续推进。 |
| 准确理解 | 把含糊要求放进同一个正常使用场景，对照各个解释会改变什么、原有能力能否继续成立。 |
| 精简实现 | 走真实调用链，按实际输入和契约决定必要校验。每个新增兜底或兼容分支都有具体用途。 |
| 准确自我迭代 | 从真实错例找最早诱发偏差的规则，用类似场景回放，保留能稳定复用的修正。 |
| 可接续的工作留痕 | 复用项目已有记录保存原始目标、关键依据、实际产物和下一动作。进度与长期知识各有归属。 |

## 开始使用

克隆后从仓库根目录打开 Codex，目录里的主规则和技能即可用于本项目。

```sh
git clone https://github.com/KamishiroRei/Evolution-Agent.git
cd Evolution-Agent
codex
```

接入其他项目时，按下方方式选用规则和技能。

把 [AGENTS.md](AGENTS.md) 放到目标项目根目录。项目已有同名文件时，把所需条款融入原有规则。想作为个人默认规则使用时，把条款合入 Codex 主目录中的 `AGENTS.md`。 [OpenAI 的 AGENTS.md 指南](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

从 [.agents/skills](.agents/skills) 选择所需的技能目录，完整复制到目标仓库的 `.agents/skills/`，或放入个人目录 `~/.agents/skills/`。可在任务中用 `$lean-coding` 等名称直接调用。 [OpenAI 的技能指南](https://learn.chatgpt.com/docs/build-skills)

| 技能 | 何时使用 |
|---|---|
| [精简编程](.agents/skills/lean-coding/SKILL.md) | 修 Bug、修改实现或审查多余的兜底、兼容分支与检查 |
| [知识管理](.agents/skills/knowledge-management/SKILL.md) | 决定什么值得长期保存，或定期检阅与精简整套规则 |
| [AgentFramework](.agents/skills/agent-framework/SKILL.md) | 从零组织或迁移 AGENT、专业技能及其加载入口 |
| [协作与独立审核](.agents/skills/agent-collaboration/SKILL.md) | 已授权的分工、跨会话接续或独立审核 |
| [Git 交付](.agents/skills/git-workflow/SKILL.md) | 需要提交、整合、推送或承接其他执行者改动 |

## 一次沟通怎样推进

以“合并两个快捷动作，整理剩余键位”为例。AI 先表达对实际效果的理解，例如合并后操作仍要连贯，界面提示要与实际按键一致。随后查绑定和提示的来源，确认合并后留下了空位，以及哪些入口还在使用原按键。

有了依据，再把重排绑定、更新提示和核对实际动作放进一份有序制作表。用户追加一项操作时，按依赖把它接入原表。简单任务可以用一句话说明目标和做法。

框架分层、实际工作例子、留痕字段与迭代方法见[框架说明](docs/framework.md)。

规则与技能均为 Markdown。许可证见 [MIT License](LICENSE)。
