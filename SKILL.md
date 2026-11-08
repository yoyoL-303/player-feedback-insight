---
name: player-feedback-insight
description: Cluster raw player feedback from community posts, reviews, surveys or customer service logs into themes, distinguish high-frequency real pain points from noise or pseudo-needs, and suggest concrete product actions. Supports plain text, Word/PDF documents, and PNG page previews. Use when the user pastes feedback, asks to analyze player comments, summarize community sentiment, 玩家反馈归类, 反馈洞察, turn messy feedback into actionable insights, or requests a document, report, or image layout version.
---

# Player Feedback Insight

## Overview

Turn messy, emotional, repetitive player feedback into a clean, prioritized insight report that a game designer or product manager can act on. Can output as structured text or as a polished downloadable document.

## Instructions

When activated:

1. Accept any form of raw feedback the user provides (community comments, app store reviews, survey answers, customer service tickets, internal notes). If the volume is large, work with what is given and note that sampling may apply.

2. Before clustering, consult these references:
   - `references/common-themes.md` for standard game industry feedback categories
   - `references/judgment-guide.md` for criteria to separate real pain points from noise or pseudo-needs
   - `references/genre-focus.md` for how feedback priorities differ by game genre (action, gacha, open world, SLG, hyper-casual, etc.)
   First try to identify the likely genre of the game being discussed, then adjust theme priority and impact assessment accordingly. Explicitly note the genre context when it affects the judgment.

3. Do not treat every complaint as equal. Explicitly separate:
   - High-frequency, high-impact pain points
   - Loud but low-impact or niche complaints
   - Feature requests that are actually workarounds for deeper problems
   - Pure venting or off-topic noise

4. Default output is structured text using this format (see also `assets/report-template.md`):

### 反馈概览
- 总条数 / 主要来源
- 整体情绪倾向（一句话）
- 最突出的 3 个主题
- 品类判断（如果可识别）

### 主题聚类
For each major theme (usually 4–7 themes):
- **主题名称**
- 出现频率（高 / 中 / 低）+ 代表性原话（1–2句，保留玩家语气）
- 这是真实痛点还是伪需求 / 噪音？简要判断理由
- 可能的产品动作（1–2条具体建议，区分「快速缓解」和「根本解决」）

### 优先处理建议
按「影响面 × 可解决性」给出前 3 个建议优先处理的问题，并说明为什么现在处理它们最划算。

### 需要警惕的信号
列出 1–3 个可能被忽视、但值得持续观察的苗头。

### 一句话总结
给产品/策划团队的最终行动建议，控制在两句话以内。

5. If the user asks for a document, report, Word, PDF, PNG, image layout, or says the text version is too plain:
   - Generate a clean professional .docx report with clear headings, tables for meta info, highlighted summary, and consistent styling.
   - Also export PDF and PNG page previews (using soffice + pdftoppm) so the user can immediately see the visual layout.
   - Keep the same analytical content as the text version.
   - Offer both the document files and the PNG previews for download.

6. Tone: professional, direct, slightly skeptical. Prefer evidence over sympathy. Avoid both “玩家都是对的” and “玩家都是无理取闹”.

7. If the feedback is too sparse or too vague to draw solid conclusions, say so clearly and list what additional data would help.

8. After the report, offer to dive deeper into one theme, generate/regenerate the document + PNG version, or compare with a previous feedback batch.
