# Sparkling Evidence · 证据驱动研讨

基于用户材料核对指标口径、比较竞争解释，并形成可检验、可修正的判断。

这是 [Sparkling](https://github.com/thePlannerIvan/sparkling) 的非官方修改版，由 Glow-Shimmering 在此 fork 中维护，不代表原作者背书。

## 使用方式

调用名：`sparkling-evidence`。适用于业务卡点、产品决策、项目复盘及研究假设讨论。材料不足时交付取证清单，不承诺直接找到单一根因。

```text
用 sparkling-evidence 帮我讨论这份材料：为什么用户满意度上升，续费却在下降？先核对指标口径，再比较可能的解释。
```

讨论会按需核查数据定义、人群与时间窗口，为竞争解释列出支持、反证和验证条件，最终输出当前判断、证据边界及下一步行动。多轮讨论按主题维护本地白板；单轮小问题不必建文件。

## 安装

```bash
npx skills add https://github.com/Glow-Shimmering/sparkling --skill sparkling-evidence
```

也可以克隆到支持 Skill 的 Agent 目录（以下为 Claude Code）：

```bash
git clone https://github.com/Glow-Shimmering/sparkling.git ~/.claude/skills/sparkling-evidence
```

无脚本运行时或审阅页依赖；不要求安装特定的研究 Skill。需要外部证据时使用运行环境已有的检索能力，无法取得的数据列入取证清单。

## 本修改版的调整

- 先核对指标口径，不把方向不同的趋势直接当作逻辑矛盾。
- 保留有依据的竞争解释，为重要假设写明可检验预测与证伪条件。
- 以证据质量比较解释，不以简洁性或故事自洽代替因果验证。
- 新证据、口径修正或推理错误出现时，允许重审已排除的解释，并记录原因。
- 保留短轮次讨论，去掉强制挑衅、每轮提问和追求顿悟的要求。
- 结论区分已知、推测和未知；研究讨论区分文献、代码、实验结果和机制假设。
- 白板按主题分开保存，避免不同议题相互覆盖。

## 来源、版本与许可

- 原项目：[thePlannerIvan/sparkling](https://github.com/thePlannerIvan/sparkling)。
- 原作者：阿祖不看 TVC；小红书同名账号；[demyth.info](https://demyth.info)；Lawyif@163.com。
- 修改日期：2026-11-05。
- 本修改版基于上游 `SKILL.md` 文件 blob `8a7417f7f5a4d19fa82321009c825bec7db2203f`。
- 许可：AGPL-3.0，完整文本见 [LICENSE](LICENSE)；保留原作者 [NOTICE](NOTICE) 和 [名称使用说明](TRADEMARK.md)。
- 上游的 [COMMERCIAL.md](COMMERCIAL.md) 为原作者的合作说明，不表示原作者为本 fork 提供支持或背书。
- 来源、版本及许可说明集中在本 README；`SKILL.md` 只包含技能定义和使用规则。
- 署名用于仓库和工作过程，默认不加入最终客户交付物。

## 文件

- [SKILL.md](SKILL.md)：技能入口、研讨规则与白板流程。
- [LICENSE](LICENSE)、[NOTICE](NOTICE)、[TRADEMARK.md](TRADEMARK.md)：保留的许可、归属和名称说明。
