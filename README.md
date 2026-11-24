# 任务深化器 · 补源法验

把已有任务的专业步骤、材料依据、方法和验收要求补齐，再生成一份可直接使用的提示词。沿用当前聊天背景，不必反复复制通用四问。

## 安装

通过 Skills CLI 安装，按提示选择使用的 AI 工具：

```sh
npx skills add xxjjjj/task-deepener --skill task-deepener
```

也可以下载仓库，将整个文件夹命名为 `task-deepener`，放进工具支持的 skills 目录。Codex 的个人目录是 `~/.codex/skills/task-deepener/`，确保其中直接包含 `SKILL.md`。

## 使用

在支持命名调用的 Codex 中输入：

```text
用 $task-deepener 深化当前任务。
```

也可以提供具体任务：

```text
用 $task-deepener 深化这个任务：评估新人销售培训是否有效。
已有材料是培训课件、考核结果和新人反馈，时间限制为两天。
```

默认先简答四问，再交付完整提示词：

| 四问 | 关注点 |
| --- | --- |
| 补 | 专家会补上的必要工作 |
| 源 | 原始记录与直接证据 |
| 法 | 可执行的方法与工具 |
| 验 | 外部检验依据与失败条件 |

随后说“按这个执行”即可继续。也可一开始要求“深化后直接执行”。执行仍取决于当前工具、材料和授权；提出验证计划不代表已经完成验证。

## 出处与改编

- **核心四问：Felix Rieseberg**，2026-10-13，[How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/) 的 Depth 部分。
- **实践参考：Lauren Tan（poteto）的 pstack /sharpen**，[cursor/plugins PR #729](https://github.com/cursor/plugins/pull/729)，参考其保留用户选择和先交付改写稿的边界。
- **中文学习笔记：URNOTKRYSTALXU（许晶晶）**，《让任务更深：一段提示词的术与道》。“补、源、法、验”是学习笔记的整理口诀，不是 Felix 的原话。公司内部笔记链接不随公开仓库发布。
- **本次封装：**结合上述材料，在 Codex 协助下加入当前对话接续、中文触发词、输出格式、材料状态和继续执行规则。

本项目是非官方中文改编，不宣称发明原方法，也不代表原作者背书。原始文章及参考项目的权利和许可归各自权利人；本仓库不替原作重新授权。转发或重新打包时请保留出处与改编说明。

## 验证范围

已通过 Skill 结构校验。尚未做与原始提示词的任务效果对照测试，不声称效果完全等同或优于原作。
