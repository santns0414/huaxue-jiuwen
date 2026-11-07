# 九年级化学 · 六维复习（人教版）

手机友好的静态复习站，对齐「语文六维解读」站点体验。

- 人教版九年级化学全一册：12 单元 · 34 课题
- 六维：核心概念 / 反应与方程式 / 实验要点与现象 / 计算与推导 / 易错与辨析 / 真题·情境应用
- **刷题**：`questions.json`（单选/判断/填空）+ 错题/难度/单元筛选；本机错题记入 localStorage
- **材料题**：独立栏 `#cailiao`，`questions-material.json` 材料套卷 + 小题；可按难度/单元筛选
- 中考趋势板块（2021–2025 备考提纲）
- 浅色 / 深色主题；笔记保存在浏览器 localStorage

## 本地预览

```bash
npx serve public
```

打开后点顶栏「刷题」`#shuati` 或「材料题」`#cailiao`。

## 题库文件（放在 `public/`）

| 文件 | 说明 |
|------|------|
| `questions.json` | 刷题主库（单选/判断/填空） |
| `questions-material.json` | 材料题套卷（type: material + subQuestions） |
| `wrong-topics.json` | 错题映射：`questionIds` 优先；否则匹配 `knowledgePoints` / `topicIds` / `tags` |
| `wrong-topic-map.json` | 化学 bot 错题主题 id 表（可选，辅助错题筛选） |

题目字段：`id, unitId, lessonId, year, source, difficulty(1/2/3), type, stem, options[{key,text}], answer, explanation, tags, knowledgePoints`。

## 部署

静态托管 `public/` 目录即可（Vercel / Cloudflare Pages 等）。
