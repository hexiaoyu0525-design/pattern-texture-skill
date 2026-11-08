# pattern-texture-skill · 服装纹样与面料肌理设计技能

![License](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)
![Version](https://img.shields.io/badge/Version-1.1.1-blue)
![Stars](https://img.shields.io/github/stars/hexiaoyu0525-design/pattern-texture-skill)

> 一套面向**服装设计师、纹样师、教师、参赛学生**的方法论：把"纹样/肌理从哪里来、怎么设计、能不能落地"一路打通——覆盖 **纹样构成、色彩构成、风格标签库、工艺适配、立体肌理、转译重构、应用部位、出图模板、版权合规、自检诊断** 十大核心能力。

> 🎨 **配套技能**：[fashion-studio](https://github.com/hexiaoyu0525-design/fashion-studio)（服装全流程：企划/出图/视频/赛事）——两个技能可独立使用，也可协同工作。

License: **CC BY 4.0**（使用须署名）· 版本 1.1.1 · 作者：hexiaoyu0525-design

---

## 这是什么

`pattern-texture-skill`（简称 PTS）是一个 **Agent Skill（智能体技能）**：一个 `SKILL.md` + 一组 `references/` 方法论文档 + `style-library/` 风格标签库。任何支持 SKILL.md 的 Agent 读到它，就会按这套规范帮你做纹样设计、肌理分类、工艺校验、转译重构、配色方案和出图提示词。

它是**方法论、检查清单、提示词骨架、工艺常识**，不是一个连了某个平台的插件，也不包含可执行代码。

### 十大核心能力

1. **纹样设计与生成提示词**：二方连续 / 四方连续 / 适合纹样 / 单独纹样的标准出图流程。
2. **面料肌理分类与生成**：提花 / 绗缝 / 扎染 / 植绒 / 面料再造等 50+ 种肌理的视觉描述。
3. **纹样工艺适配判断**：七大工艺族 + 高端/特殊工艺的可行性建议与成本量级。
4. **传统纹样现代化转译**：15 种创新模式（骨式提取、风格混搭、解构重组、材质转译、古今对话……）。
5. **配色方案生成与色彩调性判断**：三层配色比例、深浅底差异、工艺配色限制。
6. **纹样自检与质量检查**：构成 / 配色 / 工艺 / 去 AI 味四张检查清单。
7. **标准化出图提示词输出**：三步出图流程 + 五种场景模板 + 负面提示词库。
8. **非遗纹样考据辅助**：传统纹样的骨式、配色、工艺考据（拿不准的标【待核实】）。
9. **纹样解析与骨式分析**：拿到参考图后的 7 步拆解流程与输出模板。
10. **服装风格与纹样匹配指导**：部位速查、密度控制、面料适配、风格匹配。

并覆盖：纹样版权边界（传统 vs 现代品牌 vs AI 生成）、翻车诊断（症状→病因→药方）、案例参考（宋韵新生完整案例）。

### 特点

- **纯 Markdown、零代码、零专有 API**：不依赖任何平台的连接器，也不依赖本地算力。
- **工具中立**：默认用即梦 Seedream / Seedance（作者实测），但同一套方法可迁到任何生图平台。
- **"Agent 备料，你按生成"**：即使 Agent 没有图像工具，也能把构成、配色、工艺、提示词备齐，你在任意平台手动粘贴生成。
- **与 fashion-studio 协同**：FS 管服装整体（版型、廓形、模特、大片），PTS 管纹样/肌理/工艺细节；两边边界在文件开头互相声明。
- **可移植**：无写死的本地路径、无私有链接；风格标签库按东方传统 / 西方历史 / 现代当代 / 其他地区分四册。

---

## 明确不做什么（边界）

- **不做服装整体廓形与分割线设计**：那是 `fashion-studio` 的 `composition-garment.md` 负责；PTS 只负责"纹样贴在哪个部位、密度多少"。
- **不做面料本身的材质选择与再造决策**：面料选型、材料实验、可持续材料走 `fashion-studio` 的 `fabric-guide.md` 和 `material-lab.md`；PTS 只负责"纹样/图案用什么工艺做出来"。
- **不做服装整体 IP 与商用版权判定**：品牌系列、成衣版权走 `fashion-studio` 的 `copyright-compliance.md`；PTS 只负责纹样/图案层面的版权边界。
- **不做纹样百科全书式的历史长篇**：只给设计层面有用的信息，学术考据拿不准就标【待核实】。
- **不承诺精确工艺校验**（如"最小线宽 X mm"）：只给常识性建议，实际生产前必须找工厂打样。

---

## 安装

### 方式一：skills 安装器（推荐）

在支持 skills 的 Agent 环境中：

```bash
npx skills add <你的GitHub用户名>/pattern-texture-skill
```

### 方式二：手动安装

1. 下载或 clone 本仓库；
2. 把整个 `pattern-texture-skill` 文件夹放进该 Agent 的 skills 目录，例如：
   - 豆包：用户级 skills 目录（`.user_skills/`）
   - Claude Code：`~/.claude/skills/`
   - 其他：按其官方 skills / 配置入口放入同一份 `SKILL.md`
3. 重开一个新会话，Agent 即会加载。

### 不支持 SKILL.md 的 Agent / 网页对话

把 `SKILL.md` 与 `references/` 当作"手册 / 提示词包"：让它读取该目录，或把 `SKILL.md` 贴进系统提示 / 项目说明，让它按任务路由表引用对应文件。方法依然有效，只是不会自动触发。

---

## 与 fashion-studio 的分工

`fashion-studio`（FS）与 `pattern-texture-skill`（PTS）是**同作者、同许可、可独立安装、也可协同工作**的两个技能：

| 领域 | 归 FS | 归 PTS |
|---|---|---|
| 版型 / 廓形 / 分割线 | ✅ | — |
| 模特 / 大片 / lookbook | ✅ | — |
| 款式图 / 效果图 / Line-up | ✅ | — |
| **纹样构成 / 骨式 / 连续组织** | — | ✅ |
| **纹样配色 / 三层比例** | — | ✅ |
| **面料肌理分类与描述** | — | ✅ |
| **纹样工艺适配（印花/刺绣/提花）** | — | ✅ |
| **纹样贴在哪个部位、密度多少** | — | ✅ |
| 面料本身选什么材质 | ✅（`fabric-guide.md`） | — |
| 面料再造 / 材料实验 | ✅（`material-lab.md`） | — |
| 服装整体 IP / 成衣版权 | ✅（`copyright-compliance.md`） | — |
| 纹样 / 图案版权边界 | — | ✅（`copyright-guide.md`） |

**两种联动模式**：
- **FS 先行**：已完成的色彩板 / 面料板作为基础，PTS 在此基础上深化纹样设计。
- **PTS 先行**：PTS 输出的配色方案、肌理方案如果更好，可反向更新 FS 的色彩板 / 面料板。

设计是迭代的，不是单向约束。

---

## 快速开始

直接对 Agent 说一句话即可：

- 「帮我出一个四方连续的宋式折枝纹样提示词」
- 「分析一下这个丝巾纹样的骨式和配色」
- 「这个纹样能不能刺绣？成本大概多少」
- 「把传统缠枝纹转成现代极简风格」
- 「生成的纹样太满了 / 拼接不上 / 配色太艳，帮我看看怎么改」

### 示例：完整走一遍

**你说**：「帮我设计一个宋韵新生主题的春夏连衣裙纹样」

**Agent 输出**：
1. 先反问你 2-3 个问题：情绪方向（清雅/华丽/现代）、配色偏好（天青/藕荷/泥金）、工艺类型（印花/刺绣/提花）
2. 给你设计思路：用什么创新模式（比如"骨式提取 + 古今对话"）、主纹是什么、地纹是什么
3. 给你三层配色方案：主色 70% + 辅助色 20% + 点缀色 10%（带 HEX 色值）
4. 给你工艺建议：这个纹样适合什么工艺、注意什么限制
5. 给你完整出图提示词：直接复制到即梦/Midjourney 就能生成

开工可在项目文件夹放 `纹样/ 参考图/ 面料/ 灵感/` 等素材，Agent 会按 `SKILL.md` 任务路由表加载对应文件。

---

## 目录结构

```
pattern-texture-skill/
├─ SKILL.md                     # 入口：任务路由、开工方式、基本原则、输出规范
├─ README.md                    # 本文件（给人看）
├─ LICENSE                      # CC BY 4.0
└─ references/                  # 全部方法论（Agent 按需加载）
   ├─ composition-guide.md       # 构成概览（组织形式/骨式/法则/复杂度分级）
   ├─ composition-pattern.md    # 构成深度（骨式几何/四方连续/正负形/疏密）
   ├─ color-guide.md             # 配色概览（快速判断/主辅点缀/风格→配色方向）
   ├─ color-pattern.md           # 配色深度（三层比例/对比/深浅底/工艺限制）
   ├─ design-workflow.md         # 创新设计 8 步流程
   ├─ innovation-library.md      # 15 种创新模式 + 系列化方法
   ├─ translation-guide.md       # 传统元素现代化转译四种方法
   ├─ analysis-workflow.md       # 参考图 7 步拆解流程
   ├─ style-library/             # 风格标签库
   │  ├─ east-asian.md           #   东方传统
   │  ├─ western-historic.md     #   西方历史
   │  ├─ modern-contemporary.md  #   现代当代
   │  └─ global-tribal.md        #   其他地区 / 部落
   ├─ craft-guide.md             # 七大工艺族 + 高端/特殊工艺 + 成本 + 组合决策
   ├─ texture-guide.md           # 50+ 种肌理分类
   ├─ application-guide.md       # 部位速查 + 密度 + 面料适配 + 风格匹配
   ├─ prompt-templates.md        # 三步出图流程 + 五种场景模板 + 负面提示词
   ├─ quality-checklist.md       # 构成/配色/工艺/去AI味四张检查清单
   ├─ pattern-diagnosis.md       # 翻车急诊（症状→病因→药方）
   ├─ copyright-guide.md         # 纹样版权边界
   ├─ case-study.md              # 实战案例（宋韵新生 + 反向解析 + 翻车修复）
   └─ extensions/                # 非遗扩展包（可选，当前待补充）
      └─ README.md
```

---

## 生成平台与适配

- **默认**：生图用即梦 **Seedream 5.0 Pro**（大片 / 高定 / campaign 等成品档默认 Pro；Pro 不可用时降级 5.0 Flash / 标准版）。
- **可换**：Midjourney / Flux / Stable Diffusion / 其他出图平台。能力清单、术语映射、降级做法见 `fashion-studio` 的 `references/tool-adapter.md`（同一套适配层）。
- 各文件里标注的"参考图上限、比例、参数"等是**默认平台口径**，换平台以官方为准；设计流程、锚点、工艺常数不变。

---

## 许可证

本作品采用 **[Creative Commons 署名 4.0 国际许可协议（CC BY 4.0）](https://creativecommons.org/licenses/by/4.0/)** 授权。

- 你可以共享、改编、商用，但**必须署名原作者**（hexiaoyu0525-design，并注明作品名 pattern-texture-skill）、不得追加限制。
- 许可要点见 [`LICENSE`](LICENSE)（本仓库 LICENSE 为要点摘要 + 官方链接，非全文）；完整法律文本见 [CC BY 4.0 官方页面](https://creativecommons.org/licenses/by/4.0/legalcode)。

**使用边界**：本仓库公开，欢迎学习与借鉴方法论（设计思路、流程组织、检查清单均可参考）。但不得在未署名或改名换名后作为自己作品发布；引用本作品内容请注明出处。

© 2026 hexiaoyu0525-design　·　仓库：<https://github.com/hexiaoyu0525-design/pattern-texture-skill>

> 免责声明：本作品为方法论与提示词模板，以"现状"提供；涉及品牌名仅用于行业示例，不构成侵权指引；商用请遵循各生成平台条款与所在国法规。
