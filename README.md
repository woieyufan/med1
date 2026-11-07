# 台灣醫師專技高考第一階段：全科目極致速讀講義網站

本專案收錄台灣考選部「醫師專門職業及技術人員高等考試第一階段」（醫學一、醫學二）共 **9 大基礎醫學科目、82 個核心高頻章節**，並建構 **8 大器官系統跨學科整合思維鏈**。

---

## 快速部署至 GitHub Pages（雲端線上隨時閱讀）

本專案已完全配置 GitHub Actions 自動化部署工作流（CI/CD），在手機、平板、筆電均可隨時連線上網閱讀。

### 步驟 1：建立 GitHub 儲存庫並上傳
1. 登入 [GitHub](https://github.com)，點擊右上角 **New repository**。
2. 填寫儲存庫名稱（例如：`med-exam-step1`），建議設為 **Public**。
3. 將本專案的所有檔案（`docs/`、`mkdocs.yml`、`.github/`、`requirements.txt` 等）上傳或透過 Git 推送至該儲存庫：
   ```bash
   git init
   git add .
   git commit -m "Initial commit of medical exam lecture notes"
   git branch -M main
   git remote add origin https://github.com/<你的使用者名稱>/med-exam-step1.git
   git push -u origin main
   ```

### 步驟 2：啟用 GitHub Pages 自動部署
1. 進入 GitHub 儲存庫頁面，點選上方的 **Settings**（設定）。
2. 在左側選單點選 **Pages**。
3. 在 **Build and deployment** 下方的 **Source** 下拉選單中，選擇 **GitHub Actions**。
4. 設定完成！GitHub Actions 會自動偵測並開始編譯網站，約 1 分鐘後即可看到您的專屬網站網址：
   $$\text{https://<你的使用者名稱>.github.io/med-exam-step1/}$$

---

## 本地離線使用

如果需要在沒有網路的情況下離線閱讀：
1. 雙擊執行 `點此開啟講義離線網站.bat`，即可直接在瀏覽器中離線開啟完整站點。
2. 或直接開啟 `subject_handbooks/` 資料夾，查閱 9 大學科之微軟 Word (`.docx`) 與 Markdown (`.md`) 專科衝刺手冊。

---

## 目錄架構

```
├── .github/workflows/deploy.yml   # GitHub Pages 自動構建工作流程
├── docs/                          # 82 章節 Markdown 原始檔與跨科高頻專題
│   ├── index.md                   # 講義首頁與總覽
│   ├── high-yield/                # 八大器官系統跨學科整合思維鏈
│   ├── med1/                      # 醫學（一）41 章（解剖、組胚、生理、微免、寄生蟲）
│   └── med2/                      # 醫學（二）41 章（生化、藥理、病理、公衛）
├── subject_handbooks/             # 九大學科獨立 Word (.docx) 與 Markdown (.md) 專冊
├── mkdocs.yml                     # 站點架構、導覽樹與主題設定檔
├── requirements.txt               # Python 依賴清單
└── 點此開啟講義離線網站.bat       # 本機一鍵開啟離線站點捷徑
```
