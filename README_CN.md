<div align="center">

[中文](README_CN.md) · [English](README.md)

# ⭐ dreamer-star-ip

**蜂蜜黄五角星 IP × 极简概念性编辑插画。**

一张图 = 一个概念 + 大量留白 + 3 处结构性排线 + 反差抓手。

[![许可证：MIT](https://img.shields.io/badge/许可证-MIT-2ea44f?style=flat-square)](LICENSE)
![版本](https://img.shields.io/badge/版本-6.2-2ea44f?style=flat-square)
![示例](https://img.shields.io/badge/示例-9-2ea44f?style=flat-square)
[![GitHub Stars](https://img.shields.io/github/stars/yanliudesign/dreamer-star-ip?style=flat-square&label=STARS&color=f97316)](https://github.com/yanliudesign/dreamer-star-ip/stargazers)

![Claude Code Skill](https://img.shields.io/badge/Claude_Code-Skill-d97757?style=flat-square&logo=anthropic&logoColor=white)
![Codex Skill](https://img.shields.io/badge/Codex-Skill-22c55e?style=flat-square&logo=openai&logoColor=white)
![OpenCode Skill](https://img.shields.io/badge/OpenCode-Skill-3b82f6?style=flat-square)
![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-8b5cf6?style=flat-square)
![Hermes Skill](https://img.shields.io/badge/Hermes-Skill-ec6f9e?style=flat-square)

</div>

## 是什么

小星妍（Dreamer 妍妍）—— 一颗微微歪掉的蜂蜜黄五角星、头顶紧贴 "Dreamer" 小弧、右下侧一片手绘排线、随情境变形的头顶状态符号（灯泡 / `?` / 皇冠 / 云朵 / 闪电 / 星火 / 对话气泡 ...）。她**必须参与画面的核心动作**，永远不是装饰。

**适合用于**：中文公众号文章正文配图、小红书图文、幻灯片、Notion 文档、社交分享封面 —— 3:4 竖版为主，也支持 4:3 / 1:1。

**不适合**：真人封面（→ 用其它 skill）、3D 商业插画、PPT 信息图 / 架构图。

## 参考与致谢

本项目参考了 Ian 的 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations) 在中文文章认知锚点提炼、shot list 和编辑插画工作流上的实践。感谢 Ian 对这套方法的开源分享。

第三方来源与许可证信息见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

## 在原方法上增加了什么

Ian Xiaohei Illustrations 提供了一套把中文文章转成概念性编辑插画的通用工作流。dreamer-star-ip 在此基础上继续发展成强调系列一致性的角色 IP 系统：

- 完整角色规范：形态、性格、姿态、签名、配角关系与常见崩坏都有明确约束。
- 由 5 个意图族群、16 个状态符号组成的动态表达词典，用来说明角色此刻在想什么。
- 由 5 类、48 个可复用动作组成的动作库，从五角星专属隐喻到职场情境，都能直接嵌入主 Prompt 骨架。
- 面向 3:4、4:3、1:1 的量化构图规则，包括留白率、反差轴、标签上限和排线位置。
- 用于跨主题、跨图像模型保持视觉身份的 12 区块 Prompt 结构。
- P0/P1/P2 分级质量控制，明确何时重画、局部修改或接受轻微偏差。

这个项目不是 Ian 通用配图工具的替代品，而是把一个原创角色系统做得更可复用、可检查、可扩展。

## 目录结构

```
dreamer-star-ip/
├── SKILL.md                        ← 入口：核心定位 + 5 步工作流
├── references/
│   ├── style-dna.md                风格 DNA · 颜色 · 留白率 · 排线语言
│   ├── xiaoxingyan-ip.md           小星妍 IP 完整规格：形态 / 姿态库 / 禁忌
│   ├── status-glyphs.md            16 个头顶状态符号 · 5 个族群 · 挑选规则
│   ├── action-library.md            48 个可复用动作 · 5 类场景
│   ├── composition-patterns.md     构图哲学 · 反差抓手 · 尺寸规则
│   ├── prompt-template.md          单张图 12 区块英文 prompt 模板
│   └── qa-checklist.md             生成后 QA 清单 + 反 slop 规则
├── example/                        9 张成品图 · README 九宫格展示
├── action-library-preview.html     动作库可视化浏览页
├── THIRD_PARTY_NOTICES.md          上游来源与许可证声明
└── examples/
    ├── ai-era-product-interview-v6.2.md   7 张 v6.2 实例（含跳跃收尾图）
    ├── six-vertical-illustrations.md      早期 6 张
    ├── four-poses/                        姿态展示
    └── ip-manual/                         IP 手册
```

## 怎么用

### 装成 Codex skill

```bash
# Codex 全局（默认安装到 ~/.codex/skills）
CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
mkdir -p "$CODEX_HOME/skills"
ln -s "$(pwd)" "$CODEX_HOME/skills/dreamer-star-ip"
```

之后在 Codex 新对话里说：「用小星妍风格给我这篇文章配图」/「dreamer-star-ip 生成一个思考的 pose」，就会自动触发。

### 手动用作 prompt 库

不装成 skill 也行 —— 直接抄 [`examples/ai-era-product-interview-v6.2.md`](examples/ai-era-product-interview-v6.2.md) 里的 prompt 喂给你的图像模型（GPT-image / Nano Banana / Midjourney）。

### 从动作库搭建场景

打开 [`action-library-preview.html`](action-library-preview.html) 可视化浏览动作，或阅读 [`references/action-library.md`](references/action-library.md) 查看完整规格。

1. 根据主题从 48 个动作中挑一个。
2. 把对应的“动作段”复制到主 Prompt 模板的 `Single visual concept` 和 `Composition` 部分。
3. 补充 1–2 个简短中文标签，生成后再按 QA 清单检查。

动作库分为五角星专属动作、通用姿势、情境套装、表情包基底、求职职场专题 5 类。

## 示例

<table>
    <tr>
        <td><img src="example/71ceb6fd-f2c3-42c4-b419-3e87dc9a2bce.jpeg" width="240" height="320" alt="dreamer-star-ip 示例 1"></td>
        <td><img src="example/Gemini_Generated_Image_7yx70x7yx70x7yx7.png" width="240" height="320" alt="dreamer-star-ip 示例 2"></td>
        <td><img src="example/Gemini_Generated_Image_c2j3vhc2j3vhc2j3.png" width="240" height="320" alt="dreamer-star-ip 示例 3"></td>
    </tr>
    <tr>
        <td><img src="example/Gemini_Generated_Image_r5nht8r5nht8r5nh.png" width="240" height="320" alt="dreamer-star-ip 示例 4"></td>
        <td><img src="example/Screenshot%202026-07-18%20at%204.07.25%E2%80%AFPM.png" width="240" height="320" alt="dreamer-star-ip 示例 5"></td>
        <td><img src="example/Gemini_Generated_Image_w368oyw368oyw368.png" width="240" height="320" alt="dreamer-star-ip 示例 6"></td>
    </tr>
    <tr>
        <td><img src="example/be47bbf4-6d72-4e60-91fb-be46e41d7380.jpeg" width="240" height="320" alt="dreamer-star-ip 示例 7"></td>
        <td><img src="example/c29d3e5a-ec58-48a1-a1b1-9c5dad9d6762.jpeg" width="240" height="320" alt="dreamer-star-ip 示例 8"></td>
        <td><img src="example/e66317aa-5aff-4fed-a55a-6fa4eab4938e.jpeg" width="240" height="320" alt="dreamer-star-ip 示例 9"></td>
    </tr>
</table>

## 核心哲学

- **一张图 = 一个概念**。不塞信息图、不塞架构图。
- **55–65% 留白**。空白不是浪费，是让概念呼吸的地方。
- **3 处结构性排线**（同一角度）。其他一律留空 —— 排线蔓延 = 视觉噪声。
- **反差抓手**。上部 vs 下部 / 前 vs 后 / 定义 vs 优化 / 单体 vs 群体 —— 一秒能读出的对比。
- **头顶状态符号是第二眼线索**。选那个能回答"她此刻头脑里最主要的那件事是什么"的符号。
- **她永远在做一件事**。绝不立正，绝不当装饰。宁可跳一下也不要僵。

## 许可

MIT — see [LICENSE](LICENSE).

IP 视觉设计（小星妍形象、头顶状态符号系统、构图语法）欢迎学习和二创；如用于商业场景，请注明来源。
