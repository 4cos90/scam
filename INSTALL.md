# 安装指南

## 简介

「崩老头」反诈科普 Skill（anticam-blt）是一个 Claude Code Skill，用于帮助用户：
- 识别自己是否正在被「崩老头」类情感诈骗
- 帮助身边正在被骗的人
- 学习骗局的运作机制
- 报警与证据保留

## 系统要求

- Claude Code 最新版
- 一个工作目录（用于放置本 Skill）

## 安装步骤

### 方式 1：复制到 Claude Code skills 目录

```bash
# 找到你的 Claude Code skills 目录
# 通常在 ~/.claude/skills/ 或项目目录的 .claude/skills/

# 复制本 Skill 文件夹到 skills 目录
cp -r 崩老头-skill/ ~/.claude/skills/

# 或者，如果使用项目级 skills
cp -r 崩老头-skill/ .claude/skills/
```

### 方式 2：在 Claude Code 中直接引用

把整个 `崩老头-skill/` 文件夹放在你项目的根目录，然后 Claude Code 会自动发现。

### 验证安装

在 Claude Code 中输入：

```
/anticam-blt
```

或

```
/崩老头反诈
```

如果 Skill 启动，会显示欢迎消息并询问你的场景。

## 触发方式

| 输入 | 触发场景 |
|------|---------|
| `/anticam-blt` | 任意场景（中文友好） |
| `/崩老头反诈` | 任意场景（中文） |
| `/崩老头` | 任意场景（中文） |
| 「我可能遇到崩老头了」 | 自动触发 |
| 「我朋友好像被人骗了」 | 自动触发 |
| 「怎么识别情感诈骗」 | 自动触发 |

## 文件结构

```
崩老头-skill/
├── README.md           # 抽象封面（戏仿风格）
├── README_EN.md        # 英文版封面
├── SKILL.md            # Skill 主体（本 Skill 的核心定义）
├── INSTALL.md          # 本文件
├── LICENSE             # 许可证
└── prompts/
    ├── recognition.md      # 自我识别 prompt
    ├── victim_help.md      # 旁观者干预 prompt
    ├── scam_mechanics.md   # 骗局机制科普 prompt
    └── prevention.md       # 预防策略 prompt
```

## 卸载

```bash
rm -rf ~/.claude/skills/崩老头-skill/
```

或

```bash
rm -rf .claude/skills/崩老头-skill/
```

## 隐私

本 Skill **不会**上传或存储用户对话内容。所有对话都保留在你的本地 Claude Code 环境中。

如果你向 Skill 提供了聊天截图或聊天记录用于识别分析：
- 这些内容**只在你当前的 Claude Code 会话中使用**
- 不会被发送任何第三方服务器（除了 Claude API 本身处理对话）
- 不会被用于训练或改进任何模型

如果你担心隐私，可以：
- 在会话结束后清空对话历史
- 提供的截图**打码**后再发送（保留主要内容，遮蔽头像 / 昵称 / 金额）
- 直接描述情况而不提供截图

## 反馈

本 Skill 是开源反诈科普工具。如果你：
- 发现了新的骗子手法
- 想要改进某些识别模式
- 想要贡献新的 prompt

欢迎在项目仓库提 issue / PR。

## 重要提醒

⚠️ **本 Skill 是反诈工具，不是教程。**

- 它**不会**教你如何骗人
- 它**不会**复制可执行的诈骗话术
- 它**只**描述骗子行为模式，让受害者识别

如果你正在或曾经参与过诈骗活动，请：
- 拨打 **010-82951332**（北京心理危机研究与干预中心）
- 或咨询当地法律援助（12348）

**回头永远不晚。**