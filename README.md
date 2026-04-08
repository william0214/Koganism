# Koganism
### A Philosophy of Knowledge as Organism · 知識有機體哲學

> Most knowledge tools are built. This one is grown.
> 大多數知識工具是被建造的。這一套是被培養的。

---

## The Problem · 問題所在

We don't have an information shortage. We have a **digestion and immunity shortage**.
我們不缺資訊。我們缺的是**消化能力與免疫系統**。

Every PKM tool solves storage. None of them solve metabolism. None of them defend against misinformation. You collect repos you never understand, bookmark articles seeded with hallucinated facts, and build a second brain that confidently knows wrong things.
每個 PKM 工具解決儲存問題。沒有一個解決代謝問題，也沒有一個防禦錯誤資訊。你收集了從沒理解的 repo，收藏了混入幻覺事實的文章，建了一個對錯誤事情充滿自信的第二大腦。

The question isn't *how do you store knowledge*. It's *how does knowledge become you — and how do you stop bad knowledge from becoming you*.
問題不是「如何儲存知識」，而是「知識如何成為你——以及如何阻止壞的知識成為你」。

---

## Architecture · 系統架構

Two layers. One is sequential. One is always on.
兩個層次。一個是序列的。一個永遠運作。

```
┌─────────────────────────────────────────────────────┐
│              CORE SYSTEMS · 核心機制                  │
│  🔴 Immunity (免疫)    🟢 Metabolism (代謝)          │
│  Always running · cross-cutting · 貫穿全流水線        │
└─────────────────────────────────────────────────────┘
                         ↕
┌─────────────────────────────────────────────────────┐
│              PIPELINE · 流水線                        │
│  0聞 → 1攝取 → 2咀嚼 → 3消化 → 4反芻 → 5排泄 → 6累積 │
│  Sequential · ordered · 序列執行                     │
└─────────────────────────────────────────────────────┘
```

---

## Core Systems · 核心機制

### 🟢 代謝 · Metabolism · Energy & Conversion
**Knowledge transformed into project output.**
**知識轉化為專案產出。**

Metabolism is not a stage — it's the measure of whether the pipeline is working.
代謝不是某個階段——它是衡量流水線是否有效運作的指標。

- **Output rate · 產出頻率**: How often does ingested knowledge become a shipped decision, feature, or written piece?
- **RAG real-time sync · 即時更新**: The knowledge base continuously feeds a retrieval layer, keeping AI responses grounded in your latest understanding — not stale training data.

> A pipeline with no metabolic output is a storage system with extra steps.
> 沒有代謝產出的流水線，只是多了幾個步驟的儲存系統。

---

### 🔴 免疫 · Immunity · Defense & Truth Verification
**The system that keeps hallucinations out.**
**阻止幻覺進入的防禦系統。**

Immunity runs at every stage. When new information enters, the immune system challenges it.
免疫機制在每個階段運作。當新資訊進入時，免疫系統主動質疑它。

#### Protocol 1: T-Cell Response · T 細胞反應 · Cross-Validation
When Gemma 4 reads new content, it cross-references your existing knowledge base for established facts. If new information **conflicts** with known facts:

1. Conflict flagged → **Inflammation triggered** (炎症反應)
2. User notified for manual review
3. Content quarantined until resolved

```
New Info ──→ [Gemma 4] ──→ Compare with KB ──→ Conflict?
                                                    │
                                          YES ──→ 🔴 QUARANTINE
                                          NO  ──→ ✅ PROCEED
```

當 Gemma 4 讀取新內容時，與知識庫中已知事實交叉比對。若新資訊與已知事實**衝突**：立即觸發炎症反應，通知使用者人工審核，隔離內容直至確認。

#### Protocol 2: Antigen Neutralization · 抗原中和 · Source Enforcement
**No source = potential virus. Quarantine by default.**
**沒有來源 = 潛在病毒。預設隔離處理。**

Every claim extracted during Stage 3 (Digest) must carry a source link. The extraction prompt enforces this:

```
Rule: Every factual claim must include [Source: URL].
      Claims without sources are tagged [UNVERIFIED — QUARANTINE].
      Do not present unverified claims as knowledge.
```

Unsourced assertions are stored in a separate `/quarantine/` folder, never merged into the main knowledge base until manually verified.

每個在 Stage 3（消化）提取的論點必須附帶來源連結。沒有來源的論點標記為「潛在病毒」，存入隔離資料夾，不合併進主知識庫，直到人工確認。

---

## Pipeline · 流水線

### Stage 0 — 聞 · Smell · 嗅探信號

Continuously monitors: **GitHub Trending · Hacker News · X/Social Media**

Each signal scored by:
- Relevance to current focus
- Novelty (not already in KB)
- Source credibility (immunity pre-check)

Only signals above threshold proceed. Smell is cheap. Eating is expensive.
只有評分達標的信號繼續。嗅探成本低，攝取成本高。

---

### Stage 1 — 攝取 · Ingest · 觸發捕食

Full content fetched only when Stage 0 threshold is met. No speculative ingestion.
只在 Stage 0 評分達標時才抓取全文。不投機性地預先攝取。

Sources: article body · GitHub README · discussion threads
來源：文章本體 · GitHub README · 討論串

---

### Stage 2 — 咀嚼 · Chew · 結構拆解

Raw HTML → clean Markdown. Strip noise. Preserve structure.
原始 HTML → 乾淨的 Markdown。去除噪音，保留結構。

Headings · arguments · code blocks · citations — all intact.
標題 · 論點 · 程式碼區塊 · 引用——完整保留。

---

### Stage 3 — 消化 · Digest · 雙層模型閱讀

Two-pass AI extraction with **Immunity Protocol active**:

**Claude** (fast pass · 快速過濾)
→ Core claim · novelty signal · 3 key ideas

**Gemma 4** (deep pass · 深度分析)
→ Logical structure · hidden assumptions · cross-validate against KB
→ Flag conflicts → trigger T-Cell Response if needed
→ Every claim must carry source → trigger Antigen Neutralization if missing

Output: metabolized note (not a summary — shaped for *your* thinking)
輸出：代謝後的筆記（不是摘要——按照你的思考方式塑形）

---

### Stage 4 — 反芻 · Ruminate · 深度融合 *(coming soon)*

New material collides with active projects and prior notes.
Contradictions flagged. Connections surfaced.
Goal: productive friction, not tagging.

---

### Stage 5 — 排泄 · Excrete · 定時清理

**Scheduled. Automatic. Mandatory.**
**定時執行。自動化。不可跳過。**

- Outdated content → deleted
- Superseded facts → replaced
- Never-retrieved notes → flagged for removal
- Quarantine folder → reviewed, merged or permanently purged

A knowledge base that only grows is a liability.
只會增長的知識庫是負債。

---

### Stage 6 — 累積 · Accumulate · 長期智庫

What survives becomes part of your decision substrate.
Not a note you reference. A pattern you *use*.

通過所有階段的內容成為你決策底層的一部分。不是你查閱的筆記，而是你**使用**的模式。

---

## Why This Is Different · 為什麼不同

| Standard PKM | Bio-Knowledge Pipeline |
|---|---|
| Capture everything | Score before ingesting |
| Storage-first | Metabolism-first |
| Trust AI output | Immune system validates AI output |
| Notes grow forever | Active pruning + scheduled excretion |
| No anti-hallucination layer | T-Cell cross-validation + Antigen quarantine |
| You search your notes | Notes become your intuition |

---

## Status · 進度

- [x] Framework designed · 框架設計完成
- [x] Immunity Protocol specified · 免疫協議設計完成
- [ ] Stage 0: Signal scanner · 信號掃描器 (GitHub Trending + HN + X)
- [ ] Stage 1–2: Ingestion + Markdown conversion
- [ ] Stage 3: Claude + Gemma 4 digest layer with Immunity
- [ ] Stage 4: Rumination engine
- [ ] Stage 5: Automated pruning + quarantine review
- [ ] Stage 6: Accumulation metrics + RAG sync (Metabolism layer)

---

## Philosophy · 理念

Karpathy builds understanding from first principles — starting from zero, deriving everything.
Karpathy 從第一原理建立理解——從零開始，推導一切。

This framework builds intuition from **metabolized and immune-filtered signals**.
這套框架從**經過代謝與免疫過濾的信號**建立直覺。

The difference isn't depth. It's **defense**.
差別不在深度，在於**防禦**。

In an era where AI can hallucinate convincingly, a knowledge system without an immune layer is not a second brain. It's a second brain with autoimmune disease — confidently destroying itself with misinformation.
在 AI 可以令人信服地產生幻覺的時代，沒有免疫層的知識系統不是第二大腦——而是患有自體免疫疾病的第二大腦，自信地用錯誤資訊摧毀自己。

---

---

## What is Koganism · 什麼是 Koganism

**Koganism** = Knowledge + Organism + a philosophy.

Not a tool. Not a system. Not a life cycle.
An organism — something you grow, not something you build.

**Koganism** = 知識 + 有機體 + 一種哲學立場。

不是工具，不是系統，不是流程。
是一個有機體——你培養它，而不是建造它。

---

*Koganism: the belief that knowledge should behave like a living thing — metabolizing, defending, pruning, and evolving.*
*Koganism：相信知識應該像活的東西一樣運作——代謝、防禦、修剪、進化。*
