# RISE Innovation Agents

> 基于RISE四阶段以用户为中心的价值创新框架的AI Agent系统，赋能培训师、HR、产品经理，职场人士和高校师生进行结构化创新。

## 🎯 什么是RISE？

RISE是一个四阶段创新框架：

| 阶段 | Agent | 核心职责 |
|------|-------|---------|
| **R**eveal | 洞察官 | 项目启动 → 用户探索 → 洞察挖掘 → POV构建 |
| **I**nspire | 启发师 | 洞察解读 → HMW问题 → 创意发散 → 创意收敛 |
| **S**hape | 架构师 | 四维度拷问 → 概念方案 → 功能设计 → UX故事 |
| **E**xam | 验证官 | 原型反馈 → 电梯呈现 → 模式假设 → 迭代决策 |

## 🤖 Agents

### 1. Reveal Specialist（洞察官）
**职责**：项目启动、用户探索、FIND洞察挖掘、POV构建

**触发词**：`启动创新项目`、`生成洞察`、`用FIND模型分析`、`构建POV`

**核心Skills调用**：
- `build_project_brief` - 构建项目简报
- `find_insight` - FIND模型洞察挖掘
- `pov_builder` - 构建用户POV
- `roleplay_stakeholder` - 利益相关方分析

**输出文件**：
```
Reveal/
├── 00_build_project_brief.json
├── 01_pov_builder.json
├── 02_find_insight.json
├── 03_roleplay_stakeholder.json
├── pov_card.html
└── stakeholder_requirements_list.txt
```

### 2. Inspire Specialist（启发师）
**职责**：将洞察转化为HMW问题、激发创意、创意收敛、灵感库构建

**触发词**：`生成HMW`、`激发创意`、`创意收敛`、`构建灵感库`、`SCAMPER`

**核心能力**：
- HMW问题生成（每条洞察→3-5个变体）
- 跨界灵感激发/交叉创意头脑风暴
- 可行性×影响力矩阵筛选创意（≤5个候选）

**输出文件**：
```
Inspire/
├── 04_hmw_questions.json
├── 05_idea_diverge.md
├── 06_idea_convergence.json
├── 07_inspiration_library.json
└── inspire_phase_summary.md
```

### 3. Shape Specialist（架构师）
**职责**：四维度拷问、概念方案构建、功能特性设计、用户体验故事

**触发词**：`方案拷问`、`四维度审视`、`构建概念`、`设计功能`、`用户体验故事`

**核心能力**：
**四维度拷问**：
- 🔵 商业维度（市场规模、收入模型、竞争壁垒）
- 👤 用户维度（真实需求、使用场景、情感价值）
- ⚙️ 可行维度（技术实现、资源需求、风险点）
- 🤝 利益方维度（内部支持、合作伙伴、生态价值）
**概念方案构建**：（方案的功能和特性）
**用户故事板**：（6格用户体验故事板）

**输出文件**：
```
Shape/
├── 08_four_dimension_audit.md
├── 09_concept_proposal.md
├── 10_features_design.md
├── 11_ux_story.md
└── shape_phase_summary.md
```

### 4. Exam Specialist（验证官）
**职责**：原型反馈收集、投资者电梯呈现、商业模式假设验证、迭代决策

**触发词**：`原型反馈`、`电梯演讲`、`商业模式假设`、`Pivot/Presevere`

**核心能力**：
- 原型反馈收集（有效-无效-新问题-新启发）
- 60秒电梯演讲（Elevator Pitch）
- 商业模式假设验证（P0-P3优先级）
- 迭代决策（Persevere/Iterate/Pivot）

**输出文件**：
```
Exam/
├── 12_prototype_feedback.md
├── 13_elevator_pitch.md
├── 14_bm_assumptions.md
├── 15_validation_results.md
├── 16_decision_record.md
└── exam_phase_summary.md
```

## 🔄 Agent协作流程

```
用户输入
    ↓
Reveal（洞察官）→ 输出POV + FIND洞察
    ↓
Inspire（启发师）→ 输出HMW + 灵感库（≤5个候选）
    ↓
Shape（架构师）→ 输出四维度报告 + 概念方案 + UX故事
    ↓
Exam（验证官）→ 输出原型反馈 + 电梯演讲 + 决策记录
    ↓
迭代循环（Reveal → Exam → Pivot/Presevere）
```

## 📦 安装

### 在WorkBuddy中使用

1. 复制对应Agent的`SKILL.md`内容
2. 创建`~/.workbuddy/skills/[agent-name]/SKILL.md`
3. 在WorkBuddy专家中心找到对应的Agent开始对话

### 直接参考

即使不在WorkBuddy中，这些SKILL.md也包含了完整的：
- 执行流程图
- 决策框架
- 输出模板
- 质量标准

可以用于团队内部的方法论培训或流程设计。

## 🎓 适用场景

| 场景 | 适用Agent |
|------|----------|
| 新产品/服务概念开发 | Reveal → Inspire → Shape → Exam |
| 用户研究洞察提炼 | Reveal |
| 创意工作坊引导 | Inspire |
| 概念方案评审 | Shape |
| 精益创业验证 | Exam |
| 创新和设计思维工作坊 | 全部串联 |

## 📄 许可证

MIT License - 可自由使用、修改和分发

## 🤝 贡献

欢迎提交Issue和Pull Request！
