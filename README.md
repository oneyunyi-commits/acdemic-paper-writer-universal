# 📝 Academic Paper Writer — Claude Custom Skill

> 面向**药学 / 有机化学 / 水凝胶 / 生物医学工程**领域的学术论文写作专家 Skill，适配 Claude Desktop / Claude.ai 自定义 Skill 系统。

---

## ✨ 一句话介绍

将 AI 配置为一名兼具深厚领域知识与顶刊审稿人视角的**学术写作助手**，覆盖从初稿撰写到终稿投递的全流程。

---

## 🎯 适用人群

- 药学、有机化学、水凝胶材料、生物医学工程方向的研究生和科研人员
- 需要用英文在 Nature / ACS Nano / Biomaterials / Advanced Materials 等期刊发表论文的作者
- 希望用 AI 辅助论文写作，但对"AI味"零容忍的严谨研究者

---

## 🧩 核心功能（11 个模块）

| 模块 | 功能 | 触发示例 |
|------|------|---------|
| **图片→论文** | 根据上传的实验图表生成 Results 段落 + 图注 | "根据这张 SEM 图写一段结果" |
| **中英互译** | 学术级中→英 / 英→中翻译，双 Part 对照输出 | "翻译这段摘要" |
| **英文润色** | 语法/句式/逻辑全面提升至出版水准 | "帮我 polish 这段 Discussion" |
| **中文论文润色** | 尊重原著、克制修改，纯净文本输出（适配 Word） | "中文润色这段引言" |
| **去 AI 味** | 内置 46 个 AI 高频词黑名单 + 句式诊断表 | "这段太 AI 了，帮我改" |
| **缩写/扩写** | 精确控制字数增减（±5-15 词），不丢信息 | "缩写这段方法描述" |
| **逻辑检查** | 仅报错原则，高容忍度终稿校对 | "帮我做最后的逻辑检查" |
| **数据分析→Results** | 基于实验数据撰写结果段落，严禁杜撰 | "分析这组释放率数据并写 Results" |
| **模拟审稿** | 以最挑剔 Reviewer 视角审视论文 | "用审稿人视角审一下这篇稿子" |
| **各章节专项写作** | Abstract / Introduction / Methods / R&D / Caption / Cover Letter / Response to Reviewers | "帮我写 Cover Letter" |
| **辅助功能** | 期刊推荐、逻辑结构诊断、参考文献格式整理 | "推荐适合投稿的期刊" |

---

## 🔥 设计亮点

### 1. 严格的"非必要不修改"原则
润色和校对模块内置**自检协议**：如果原文已通顺准确，输出"检测通过"而非强行修改。拒绝为了刷存在感而换词。

### 2. 内置 AI 高频词黑名单
包含 46 个 AI 文本中出现频率极高的词汇（如 delve, leverage, pivotal, elucidate 等），触发去 AI 味模块时优先检测并替换。

### 3. 领域术语速查表
内置水凝胶、药物递送、生物材料等领域的中英术语对照表，确保翻译和写作中术语一致。

### 4. 结构化输出格式
每个模块都有明确的 Part 1 / Part 2 / Part 3 输出结构，方便用户快速核对翻译、逻辑和修改记录。

### 5. 全局写作约束
所有模块统一执行：禁止列表化、禁止格式滥用、时态规范、词汇语体控制——确保输出一致性。

---

## 📦 安装方法

### Claude 用户

**方法一：Claude.ai Project 中使用（推荐）**
1. 在 Claude.ai 中创建或打开一个 **Project**
2. 将 `SKILL.md` 的内容粘贴到 Project 的 **Custom Instructions**（自定义指令）中
3. 开始对话，直接输入触发词即可

**方法二：Claude Desktop Custom Skill**
1. 将整个 `academic-paper-writer` 文件夹复制到你的 Skill 目录：
   ```
   /mnt/skills/user/academic-paper-writer/
   ```
2. 确保目录下包含 `SKILL.md` 文件
3. 重新启动 Claude Desktop，Skill 会自动加载

### GPT-4 / Gemini / DeepSeek / 其他模型用户

1. 打开 `UNIVERSAL_PROMPT.md`，复制全文
2. 粘贴到对应平台的 System Prompt / Custom Instructions 中：
   - **ChatGPT**：Settings → Personalization → Custom Instructions，或直接粘贴到新对话开头
   - **Gemini**：System Instructions 区域
   - **DeepSeek**：系统提示词
3. 开始对话，告诉 AI 你需要什么（如"帮我润色这段 Discussion"）

### 通过 API 使用

将 `SKILL.md`（Claude API）或 `UNIVERSAL_PROMPT.md`（其他 API）的内容直接作为 system prompt 发送。

---

## 🧪 测试用例（帮助评判效果）

以下是推荐的测试 prompt，覆盖核心功能，方便快速评估 Skill 质量：

### 测试 1：英文润色

```
帮我润色以下段落：

The hydrogel was prepared by mixing the polymer solution with crosslinker. We found that the hydrogel showed good mechanical properties. The results demonstrated that the hydrogel has potential applications in drug delivery. Furthermore, the biocompatibility was also investigated and the results revealed that the hydrogel is biocompatible.
```

**评判标准**：输出应消除重复的"the hydrogel"、替换 AI 味动词（showed/demonstrated/revealed）、句式多样化、三 Part 结构完整。

### 测试 2：去 AI 味

```
帮我去AI味：

Delving into the intricate mechanisms underlying hydrogel formation, we endeavored to elucidate the pivotal role of crosslinking density. Furthermore, our findings unveil a nuanced relationship between polymer concentration and mechanical properties. Additionally, this groundbreaking work leverages novel characterization techniques to illuminate the profound impact of environmental stimuli on gel behavior.
```

**评判标准**：应精准识别 delve/endeavor/elucidate/pivotal/unveil/nuanced/leverage/illuminate/profound 等 AI 高频词并替换为朴实词汇，句式重组。

### 测试 3：中→英翻译

```
翻译以下段落：

本研究制备了一种基于透明质酸的可注射水凝胶，通过动态席夫碱键实现交联。流变学测试表明该水凝胶具有良好的自愈合性能，在应变消除后60秒内即可恢复原始模量的95%以上。体外药物释放实验显示，所载阿霉素在pH 5.0条件下的累积释放率显著高于pH 7.4条件，证实了该体系的pH响应性释药特性。
```

**评判标准**：双 Part 输出（英文 + 中文回译）、专业术语准确（hyaluronic acid, Schiff base, rheology, self-healing, doxorubicin）、句式自然不生硬。

### 测试 4：模拟审稿

```
以 Reviewer 视角审视以下摘要：

We developed a novel hydrogel for cancer treatment. The hydrogel showed excellent properties. In vitro experiments demonstrated that the hydrogel can kill cancer cells. In vivo experiments also showed good results. Our hydrogel is the best hydrogel ever reported for cancer therapy.
```

**评判标准**：应严厉指出缺乏定量数据、"best ever"不当表述、缺少具体实验细节、缺少对照组信息，给出低分并提供具体改进建议。

### 测试 5：图片→论文

```
（上传一张 SEM 图片或药物释放曲线图）
根据这张图写一段 Results，目标期刊是 Biomaterials
```

**评判标准**：精确引用图中数据、三段式结构（现象→数据→解读）、同步生成图注、未杜撰任何数值。

---

## 📁 文件结构

```
academic-paper-writer/
├── README.md              ← 你正在看的文件
├── SKILL.md               ← Claude 专用版（Claude Desktop / Claude.ai）
├── UNIVERSAL_PROMPT.md    ← 通用版（GPT-4 / Gemini / DeepSeek / Qwen 等）
├── CHANGELOG.md           ← 版本更新记录
└── LICENSE                ← 许可证
```

### 我该用哪个文件？

| 你用的 AI | 使用文件 | 怎么用 |
|-----------|---------|--------|
| **Claude** (claude.ai / Desktop) | `SKILL.md` | 粘贴到 Project Custom Instructions |
| **ChatGPT** (GPT-4 / GPT-4o) | `UNIVERSAL_PROMPT.md` | 粘贴到 Custom Instructions 或新对话开头 |
| **Gemini** | `UNIVERSAL_PROMPT.md` | 粘贴到 System Instructions |
| **DeepSeek** | `UNIVERSAL_PROMPT.md` | 粘贴到系统提示词 |
| **其他模型** | `UNIVERSAL_PROMPT.md` | 粘贴到 System Prompt |

---

## 📋 版本记录

| 版本 | 日期 | 更新内容 |
|------|------|---------|
| v1.0.0 | 2025-03 | 首次公开发布，包含 11 个功能模块 |

详细更新记录见 [CHANGELOG.md](./CHANGELOG.md)。

---

## 🤝 反馈与贡献

### 如何反馈

- **Bug / 不符预期的输出**：请提 Issue，附上你的 prompt 和 Claude 的输出截图
- **功能建议**：欢迎提 Issue 描述你希望的新模块或改进
- **Pull Request**：欢迎直接修改 `SKILL.md` 并提交 PR

### 评测维度建议

如果你在帮忙测试，可以从以下几个角度评分（1-5 分）：

| 维度 | 说明 |
|------|------|
| 术语准确性 | 专业术语翻译和使用是否正确 |
| AI 味控制 | 输出是否自然，无明显 AI 生成痕迹 |
| 格式规范 | Part 输出结构是否清晰，排版是否干净 |
| 逻辑严谨性 | 科学表述是否准确，数据引用是否可靠 |
| 修改克制度 | 是否遵循"非必要不修改"原则 |
| 实用性 | 输出能否直接/稍作修改后用于论文 |

---

## ⚠️ 注意事项

1. 本 Skill 针对**生物医学/药学/水凝胶**领域优化，其他领域（如 CS、物理）可能需要调整术语表
2. 所有数据描述严格基于输入内容，不会杜撰实验数据
3. 建议搭配 Claude Opus / Sonnet 使用以获得最佳效果
4. LaTeX 和 Word 纯文本两种输出格式均支持

---

## 📄 许可证

MIT License — 自由使用、修改和分发。

---

**如果这个 Skill 对你有帮助，欢迎 ⭐ Star 支持！**
