# Taiwan Stock Wiki 異動紀錄 (Log)

本文件依據 `AGENTS.md` 規範，遵循 **Append-only** 原則記錄整個 Wiki 的建置、資料匯入（Ingest）、知識查詢（Query）、個股研究（Research）與知識庫檢查（Lint）歷程。

---

## [2026-11-24] ingest | 台股入門原始教學文件匯入

- **新增頁面**：
  - `wiki/basics/stock-basics.md`（股票基本概念）
  - `wiki/market/tw-market-system.md`（台灣股票市場與交易制度）
  - `wiki/technical-analysis/candlestick.md`（K線圖入門）
  - `wiki/technical-analysis/volume.md`（成交量與價量關係）
  - `wiki/technical-analysis/moving-average.md`（移動平均線 MA）
  - `wiki/technical-analysis/rsi.md`（相對強弱指標 RSI）
  - `wiki/technical-analysis/macd.md`（平滑異同移動平均線 MACD）
  - `wiki/risk-management/investment-risks.md`（股票投資風險類型與辨識）
  - `wiki/risk-management/information-verification.md`（投資資訊查證與官方管道）
- **更新頁面**：
  - `wiki/index.md`（初始化分類知識總索引，建置四大主題導覽）
  - `wiki/research-backlog.md`（建立完整的台股待研究清單，涵蓋交易制度細節、基本面、籌碼面、KD指標、個股研究與ETF）
  - `wiki/log.md`（登錄本次匯入作業）
- **資料來源**：
  - `raw/articles/01_股票基本概念.txt`
  - `raw/articles/02_台灣股票市場與交易制度.txt`
  - `raw/articles/03_K線圖入門.txt`
  - `raw/articles/04_成交量與技術指標.txt`
  - `raw/articles/05_投資風險與資訊查證.txt`
- **主要整理內容**：
  1. 完整遵循 `AGENTS.md` 規範建立原子化 Wiki 頁面，每頁具備規範之 YAML Frontmatter 與 8 個標準章節。
  2. 將原始文件內容擴展為適合初學者的通俗教學語言，融入生活化說明與關鍵迷思澄清（如紅K不等於漲、超買不等於必跌、均線落後性與鈍化現象）。
  3. 嚴守金融規範，杜絕捏造數據，強調技術指標絕非保證獲利，並確立以官方公開資訊（TWSE、MOPS、TPEx、SFI）為準的資訊查證機制。
  4. 建立頁面間的 Obsidian 雙向 Wiki Links，並盤點台股交易細節、基本面三大報表、籌碼面三大法人、KD指標等後續知識缺口至 backlog。

## [2026-11-24] research | 互動式教學簡報建置 (slides/index.html)

- **新增成果**：`slides/index.html`（台股投資入門：從零開始學會看懂股票）
- **簡報頁數**：共 10 頁，純 HTML5 + CSS3 + Vanilla JS，支援電腦鍵盤導航與行動端手勢滑動。
- **引用 Wiki 頁面**：
  - `wiki/index.md`
  - `wiki/basics/stock-basics.md`
  - `wiki/market/tw-market-system.md`
  - `wiki/technical-analysis/candlestick.md`
  - `wiki/technical-analysis/volume.md`
  - `wiki/technical-analysis/moving-average.md`
  - `wiki/technical-analysis/rsi.md`
  - `wiki/technical-analysis/macd.md`
  - `wiki/risk-management/investment-risks.md`
  - `wiki/risk-management/information-verification.md`

## [2026-11-24] research | 知識圖譜導覽簡報架構升級 (Graph-based Presentation)

- **執行流程**：
  1. **階段一（抽取）**：剖析 Wiki 知識庫，抽取 10 個核心概念節點與 18 條關係邊（前置依賴、衍生計算、指標互證、風控警示）。
  2. **階段二（路徑）**：規劃主幹拓撲故事線（Primary Narrative Path）與網狀分支跳轉點。
  3. **階段三（合成）**：建立包含「核心看板、圖譜關聯跳轉（Next-Hops）、深入鑽取抽屜（Drill-down）」之三層節點卡片。
  4. **階段四（雙模態引擎）**：升級 `slides/index.html`，支援模式 A（單頁沉浸式卡片）與模式 B（SVG 全域星系圖譜），快捷鍵 `G` 自由切換。
  5. **階段五（驗證）**：執行圖譜拓撲完整性與 Wiki 來源驗證，全數通過。
- **產出檔案**：
  - `slides/graph-data.json`（知識圖譜數據規格）
  - `slides/index.html`（雙模態 Graph 互動簡報）
