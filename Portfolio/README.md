# Portfolio — 葉嘉靖

Data Analyst / Business Analyst 作品集網站。純靜態網站（HTML/CSS/少量 JS），不需要建置工具，可直接開啟或部署到任何靜態網站託管服務。

## 結構

```
Portfolio/
├── README.md
├── index.html                     ← 首頁（終端機主題的個人簡介 + 專案列表）
│
├── projects/
│   ├── bank-customer-insight/     ← 01 銀行零售客戶洞察平台
│   │   └── index.html
│   ├── vtuber-analysis/           ← 02 VTuber 觀眾問卷調查分析
│   │   └── index.html
│   ├── ta-grade-system/           ← 03 助教課成績管理系統
│   │   └── index.html
│   ├── long-covid/                ← 04 長新冠危險因子統合回歸研究
│   │   ├── index.html
│   │   └── long-covid-thesis.pdf
│   └── line-business-card/        ← 05 賴哩來 LINE 數位名片系統
│       ├── index.html
│       ├── line-digital-card-report.pptx
│       └── assets/                （簡報節錄圖片）
│
└── assets/                        （首頁共用素材，目前保留擴充用）
```

每個 `projects/*/index.html` 都是可以獨立開啟的完整頁面，彼此之間用相對路徑連結，所以整個資料夾可以直接部署（不需要伺服器端邏輯）。

## 之後要記得補的地方

1. **聯絡資訊**：`index.html` 最下面的 `contact --info` 區塊目前是佔位資料，搜尋檔案中的 `TODO` 註解，換成你的 Email / GitHub / LinkedIn。
2. **新增專案**：之後有新專案時，在 `projects/` 底下新增一個資料夾（例如 `projects/new-project/index.html`），再到首頁 `index.html` 的 `<ol class="project-list">` 裡照現有格式加一個 `<li class="project-item">` 項目即可，编号 `01, 02, 03…` 直接照順序往下寫。
3. 目前每個專案頁的視覺風格不完全相同（01–03 沿用你原本三份報告各自的設計，04–05 沿用首頁的終端機主題）——這是刻意保留的，讓每個案例可以有自己的呈現方式，但都用首頁的左上角「← Portfolio」連結串起來。

## 部署

這是純靜態網站，可以直接用以下任一方式上線：

- **GitHub Pages**：把整個資料夾內容 push 到 GitHub repo，在 repo Settings → Pages 選擇分支即可。
- **Netlify / Vercel**：直接把資料夾拖曳上傳，或連接 GitHub repo 自動部署。
- **本機預覽**：直接用瀏覽器開啟 `index.html` 即可（部分瀏覽器對本機 PDF/檔案連結有安全限制，建議用 `python3 -m http.server` 等簡易伺服器本機測試）。
