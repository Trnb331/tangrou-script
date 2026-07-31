# tangrou-script

一个先通过分轮问答了解账号、观众、业务和表达风格，再诊断口播方向并生成完整口播文案的 Agent Skill。支持开头优化、逻辑延续检查、标记式改稿和标题生成。

**支持：豆包、WorkBuddy、Claude Code、Codex，以及其他支持 Skills 的 Agent。**

本仓库以开放的 `SKILL.md` 目录格式发布。支持 Agent Skills 的 AI 可以安装整个仓库；不支持 Skills 的网页 AI 可以读取或粘贴 `UNIVERSAL_PROMPT.md`。

[下载可上传安装包：tangrou-script.zip](https://github.com/Trnb331/tangrou-script/releases/download/v1.6.0/tangrou-script.zip)

## 能做什么

- 从零访谈并建立账号底稿
- 每轮只推进一个当前任务，并根据真实反馈选择下一步
- 复用当前对话中已经确认的信息
- 诊断选题与已有初稿
- 按任务调用内容设计、对标分析和情绪洞察知识
- 内置 8 个非商业分享的原始知识包，共 1808 个知识原子
- 内置平台合规检查，自动规避测算、运势、占卜、算命、改运及变相引流
- 判断 60 秒、2 分钟或 2 分 30 秒的合适结构
- 五维诊断表格：文字洁癖、封面/标题、表达效率、认知落差、AI 辅助，带 ✅/⚠️/❌ 判断
- 诊断确认后生成完整口播逐字稿
- 开头优化：三种方法各生成 3–5 条，选出 Top 3
- 逻辑延续检查：逻辑衔接、信息密度、口播流畅度三维扫描
- 标记式改稿：保留原文，用删除线和 🆕 标记改动
- 标题生成：按平台特性生成 5–8 个方案
- 内置核心哲学：文字洁癖、先有产品后有内容、注意力劫持、投入×理解
- 犀利说话风格：不讨好、不鸡汤、不说废话、给行动不给建议
- 特别警告：遇到常见误区（纠结标题、想做干货、没有产品等）直接指出
- 内联案例库：正面和反面案例，用实战验证原则

## 安装

### 豆包与 WorkBuddy

把本仓库地址交给 Agent，并发送：

```text
请安装并使用这个 Skill。若当前产品不能直接安装 GitHub Skill，请读取 SKILL.md 和 references 目录，严格按照其中的流程执行。
```

### Codex

在 Codex 中发送：

```text
$skill-installer 安装这个 Skill：
https://github.com/Trnb331/tangrou-script
```

也可以把仓库复制到：

```text
~/.codex/skills/tangrou-script
```

### Claude Code

把仓库复制到：

```text
~/.claude/skills/tangrou-script
```

### claude.ai

从本仓库 Releases 下载 `tangrou-script.zip`，然后在 Claude 的 Skills 设置中上传。

### ChatGPT

从本仓库 Releases 下载 `tangrou-script.zip`，在支持个人 Skills 的 ChatGPT 工作区上传安装。

### Gemini CLI

```bash
gemini skills install https://github.com/Trnb331/tangrou-script
```

也可以复制到：

```text
~/.gemini/skills/tangrou-script
```

### Qwen Code

把仓库复制到：

```text
~/.qwen/skills/tangrou-script
```

也可以直接告诉 Qwen Code：

```text
请从 https://github.com/Trnb331/tangrou-script 安装 tangrou-script Skill。
```

### 其他 AI

如果 AI 没有 Skill 安装功能：

1. 打开或上传 `UNIVERSAL_PROMPT.md`。
2. 告诉 AI："严格按照这份提示词执行，先问我，再诊断口播方向，诊断确认后生成完整文案。"

## 调用

支持斜杠调用的 AI：

```text
/tangrou-script
```

自然语言调用：

```text
使用 tangrou-script，先通过问答了解我的账号和业务，再诊断这条口播应该怎么做，诊断确认后帮我写完整文案。
```

## 文件说明

```text
SKILL.md                              核心工作流（诊断 + 创作）
references/interview-map.md           分轮问诊地图
references/script-framework.md        口播结构与时长标准
references/script-writing.md          口播文案写作标准
references/hook-optimization.md       开头优化标准
references/script-flow-check.md       逻辑延续检查与标记式改稿
references/historical-workflow.md     工作流设计依据
references/single-step-routing.md     单步推进与任务切换规则
references/content-design.md          选题、平台表达与转化设计
references/platform-compliance.md     平台封建迷信禁区、合规改写与规则来源
references/benchmark-analysis.md      对标账号筛选与分析
references/insight-angles.md          情感、焦虑、人性与反认知角度
references/knowledge-pack/            8 个按需检索的第三方原始知识包
agents/openai.yaml                    OpenAI 产品界面元数据
UNIVERSAL_PROMPT.md                   不支持 Skills 的 AI 使用
```

## 许可

本仓库原创的 Skill 工作流使用 MIT License。

`references/knowledge-pack/` 中的第三方原始知识包来自 [dontbesilent2025/dbskill](https://github.com/dontbesilent2025/dbskill)，继续使用 CC BY-NC 4.0 许可：必须保留署名，只允许非商业使用、修改和分享。详细说明见该目录的 `SOURCE.md` 与 `LICENSE`。
