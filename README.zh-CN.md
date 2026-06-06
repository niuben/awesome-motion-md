# awesome-motion.md

一个 `MOTION.md` 精选集合，用来帮助 AI Agent 生成更有视觉冲击力、不呆板的 UI 动画。

## 这是什么？

`MOTION.md` 是写给 Cursor、Claude Code、OpenCode 等 AI 编程 Agent 的动画设计规则文档。

它不是简单地告诉 AI “加点动画”，而是提供一套明确的运动规范：缓动曲线、动画时长、入场动画、悬停状态、滚动触发、退出动画、可访问性规则和禁止项。

## 项目结构

```txt
awesome-motion-md/
├── src/                  # 各种动画风格规则
├── docs/                 # 使用指南与示例
├── README.md             # 英文 README
└── README.zh-CN.md       # 中文 README
```

## 动画风格

所有动画风格会放在 `src/` 目录中，每个风格都是一个完整独立的 `MOTION.md` 规则文件。

示例：

```txt
src/
├── high-impact/MOTION.md
├── elegant/MOTION.md
├── glitch/MOTION.md
└── fluid/MOTION.md
```

## 目标

让 AI 生成的界面不再只有平淡的 `fadeIn`，而是拥有明确风格、节奏和表现力的动效系统。
