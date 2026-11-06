# Sparkling Evidence · 证据驱动研讨

带着材料一起拆问题：先核对口径，再比较解释，最后明确当前判断和下一步验证。

这是 [Sparkling](https://github.com/thePlannerIvan/sparkling) 的非官方修改版，由 [Glow-Shimmering](https://github.com/Glow-Shimmering) 在此 fork 中维护，不代表原作者背书。

## 适合什么时候用

| 场景 | 讨论重点 |
| --- | --- |
| 业务卡点 | 指标变化是否可比，哪些解释有证据支持 |
| 产品决策 | 用户问题、设计假设与需要验证的取舍 |
| 项目复盘 | 当时的判断依据、反证和后续改进 |
| 研究假设 | 区分文献、代码、实验结果与推测机制 |

普通知识问答、常规代码排错和直接执行任务通常不需要这套研讨流程。它不代替真实调研或实验，也不承诺找出单一根因。

## 安装

```bash
npx skills add https://github.com/Glow-Shimmering/sparkling --skill sparkling-evidence
```

也可以克隆到支持 Skill 的 Agent 目录（以下为 Claude Code）：

```bash
git clone https://github.com/Glow-Shimmering/sparkling.git ~/.claude/skills/sparkling-evidence
```

技能入口只有一个 [SKILL.md](SKILL.md)，没有脚本、审阅页或其他 Skill 依赖。需要最小本地副本时，将该文件放入 Agent 的 `sparkling-evidence/` 技能目录即可；来源、修改记录和许可说明保留在本仓库。

## 怎么开始讨论

正式调用名为 `sparkling-evidence`。在支持显式 Skill 调用的环境中，可这样写：

```text
用 $sparkling-evidence 和我讨论：为什么用户满意度上升，续费却下降？
以下是数据和统计口径。先核对口径，再比较解释，暂时不写方案。
```

也可以用自然语言指明技能名称。不同 Agent 的加载方式可能不同；以正式名称调用，避免将 `sparking` 的拼写误差当成固定别名。

另外两个例子：

```text
用 sparkling-evidence 帮我复盘这次产品改版。
下面是原设计目标、用户反馈和使用数据，先检查哪些设计假设不成立。
```

```text
用 sparkling-evidence 讨论这组消融实验。
请区分结果能够支持的结论、尚未验证的机制，以及最有价值的下一步实验。
```

有材料时提供来源、关键观察和想解决的问题即可，不需要填固定问卷。只有话题也可以开始，先澄清一个具体场景或待做决定。

## 讨论方式与交付

1. **核对口径**：检查指标定义、人群、时间窗口、样本选择和数据来源。
2. **比较解释**：为有依据的候选解释列出支持、反证、未知和可检验预测。
3. **推进讨论**：默认短轮次交流，需要用户输入时聚焦一个关键问题。
4. **记录变化**：多轮讨论按主题维护白板，新证据可以修正此前判断。
5. **形成交付**：给出当前判断、证据边界，以及能够区分解释的验证或行动。

材料不足时，输出具体取证清单；无需强行产生“顿悟”或宣布“底层真相”。

多轮讨论可能在当前项目目录创建 `sparkling-whiteboard-<主题>.md`，单轮小问题不必建文件。白板包含讨论内容，应按项目资料管理；本仓库默认忽略这些生成文件。不可写文件时，改用对话内摘要。

## 相对原版的调整

- 先核对口径，不强制制造矛盾、挑衅或每轮提问。
- 保留竞争解释，并明确什么证据会使其降权或被否定。
- 简洁性仅作为辅助标准，不以故事自洽代替因果验证。
- 允许新证据、口径修正或原推理错误触发重新评估。
- 结论区分已知、推测和未知，支持按证据修订。

## 来源、修改记录与许可

- 原项目：[thePlannerIvan/sparkling](https://github.com/thePlannerIvan/sparkling)。
- 原作者：阿祖不看 TVC；小红书同名账号；[demyth.info](https://demyth.info)；Lawyif@163.com。
- 2026-11-05：形成证据驱动修改版，基于上游 `SKILL.md` 文件 blob `8a7417f7f5a4d19fa82321009c825bec7db2203f`。
- 2026-11-06：整理流程结构、补充缺少初始材料时的处理方式、明确引用要求，完善使用示例及白板忽略规则。
- 许可：AGPL-3.0，完整文本见 [LICENSE](LICENSE)；原作者信息见 [NOTICE](NOTICE)，名称使用说明见 [TRADEMARK.md](TRADEMARK.md)。
- 保留的 [COMMERCIAL.md](COMMERCIAL.md) 是原作者的合作说明，不表示原作者为本 fork 提供支持或背书。
- 来源、版本和许可说明放在本 README；`SKILL.md` 仅包含技能定义与使用规则。默认不在最终客户交付物中加入项目品牌或署名。

本次整理已校验 Skill 格式；尚未进行跨 Agent 或真实研讨效果评测。
