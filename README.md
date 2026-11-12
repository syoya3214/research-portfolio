# Research Portfolio
 
三石 翔也（Shoya Mitsuishi）
青山学院大学大学院 理工学研究科 理工学専攻 知能情報コース 大原研究室（修士1年）
 
研究の資料をまとめたリポジトリです。
 
---
 
## 1. Mamba-2 の状態キャッシュを重要度に応じて量子化する研究（修士・進行中）
 
言語モデル Mamba-2 が生成中に持ち続ける状態キャッシュは、生成時のメモリの大半を占めます。
本研究では、この状態の各要素を重要度で順位付けし、重要な要素には多くの bit を、重要でない要素には少ない bit を割り当てる量子化手法を提案しています。
 
- 同じメモリ量（平均 4 bit）で、一律 4 bit より高い精度を実現
- 一律 4 bit による perplexity の悪化の 72〜87% を解消（130M〜1.3B の 4 サイズ）
- bit の配分は事前に 1 回決めるだけでよく、生成中の見直しは不要
資料：[研究概要スライド（PDF）](mitsuishi_research_overview_20261112.pdf)
 
---
 
## 2. LLM を用いた逐次検索型 Multi-hop QA における回答根拠の明示的管理（学部）
 
*LLM-Based Explicit Answer Evidence Management for Sequential Retrieval Multi-hop QA*
 
複数の文書をたどって答える逐次検索型 Multi-hop QA では、検索と推論を繰り返すうちにループに陥ることがあり、その原因が分からないという課題がありました。
本研究では、回答に必要な情報を「スロット」として明示的に管理し、どの情報が取れていて推論がどこで止まっているかを追跡できるようにしました。
 
- HotpotQA・MuSiQue で評価（検索：BM25、LLM：GPT-4o）
- 必要な情報の一部が取れている場合でもループが発生することを明らかにした
- FIT2026（第25回情報科学技術フォーラム）で発表し、[FIT奨励賞](https://www.ipsj.or.jp/award/fit-syorei.html)を受賞
資料：[予稿（PDF）](m_mitsuishi_FIT_2026.pdf)
