# tangrou-script

一个先通过分轮问答了解账号、观众、业务和表达风格，再生成可直接拍摄的中文短视频口播逐字稿的 Agent Skill。

**支持：豆包、WorkBuddy、Claude Code、Codex，以及其他支持 Skills 的 Agent。**

本仓库以开放的 `SKILL.md` 目录格式发布。支持 Agent Skills 的 AI 可以安装整个仓库；不支持 Skills 的网页 AI 可以读取或粘贴 `UNIVERSAL_PROMPT.md`。

## 能做什么

- 从零访谈并建立账号底稿
- 复用当前对话中已经确认的信息
- 生成选题矩阵
- 按 60 秒、2 分钟或 2 分 30 秒结构写完整逐字稿
- 输出带时间段版本和无标注提词器版本
- 根据“太软、太空、AI 味、转化生硬”等反馈重写

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
https://github.com/OWNER/tangrou-script
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
gemini skills install https://github.com/OWNER/tangrou-script
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
请从 https://github.com/OWNER/tangrou-script 安装 tangrou-script Skill。
```

### 其他 AI

如果 AI 没有 Skill 安装功能：

1. 打开或上传 `UNIVERSAL_PROMPT.md`。
2. 告诉 AI：“严格按照这份提示词执行，先问我，再写口播。”

## 调用

支持斜杠调用的 AI：

```text
/tangrou-script
```

自然语言调用：

```text
使用 tangrou-script，先通过问答了解我的账号和业务，再为我写口播文案。
```

## 文件说明

```text
SKILL.md                         核心工作流
references/interview-map.md     分轮问诊地图
references/script-framework.md  口播结构与质量标准
references/historical-workflow.md  工作流设计依据
agents/openai.yaml              OpenAI 产品界面元数据
UNIVERSAL_PROMPT.md             不支持 Skills 的 AI 使用
```

## 许可

MIT License。允许使用、修改和分享，保留许可证即可。
