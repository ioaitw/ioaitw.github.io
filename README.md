# IOAI Taiwan ｜ 國際人工智慧奧林匹亞競賽 臺灣國家代表隊網站

靜態網站，7 個頁面，極簡風格（仿台灣語奧 ioltw.github.io）：

- `index.html` — 首頁（hero + 6 格入口 + 主辦單位 bar）
- `news.html` — 最新消息（時序列表）
- `about.html` — 關於 IOAI（賽事介紹、賽制、歷屆地點）
- `results.html` — 歷年表現（2024 / 2025 / 2026 卡片）
- `faq.html` — 常見問題（4 大類，可摺疊）
- `organizer.html` — 籌辦單位（主辦資訊、核心團隊、聯絡資訊）
- `register.html` — 報名方式（三階段流程、資格、初選筆試、遴選機制）

## 部署

純靜態檔案，可直接：
- 上傳到任何靜態主機（Netlify、Vercel、GitHub Pages、學校網站空間）
- 本機預覽：`python3 -m http.server 8080`

## 客製化

### 顏色主題
集中在 `css/style.css` 開頭的 `:root`：

```css
--c-primary: #2563eb;       /* 主色 藍 */
--c-primary-dark: #1e40af;
--c-accent: #0ea5e9;        /* 強調色 */
```

### 字體
Noto Sans TC（繁中）+ Inter（英數），由 Google Fonts CDN 載入。

### 報名連結
報名 CTA 目前指向 `news.html`（佔位）。取得 Google Form 連結後，
在 `register.html` 的「報名管道」區塊與 `news.html` 的「初選報名即將開放」項目
替換對應內容即可。

### 內容更新
- 主辦團隊：`organizer.html`「核心團隊」區
- 歷年成績：`results.html`，每屆一個 `.year-card`
- FAQ：`faq.html`，依分類在 `.faq-cat` 後新增 `.faq-block`
- 最新消息：`news.html`，依序新增 `.news-item`

## 已知事項

- 表單元件未內建：報名建議直接用 Google Form
- Logo 用文字「IOAI Taiwan」；有正式 logo 圖檔可放 `images/logo.png` 替換 `.brand-mark` 區塊
- 信箱 `ioai-taiwan@cs.ncu.edu.tw` 為示意，待正式信箱核發後替換
"# ioaitw.github.io" 
