# 《忍者喵喵》同人小說錄 (Nyannyan Shinobi Novel)

這是一個採用**純文字與前端程式碼完全分離架構**的輕小說閱讀網站，可直接上傳至 **GitHub** 並透過 **GitHub Pages** 或 **Netlify** 免費部署上線。

## 📁 專案目錄結構

```text
nyannyan-shinobi-novel/
├── index.html               # 網站主程式（負責排版、燈箱看圖、手機防變形導航與動態載入文字）
├── README.md                # 專案說明與後續新增章節教學
├── images/                  # 插圖素材資料夾
│   ├── kunoichi_view.jpg    # 第二節：低角度仰視插圖
│   ├── cg_sakura.jpg        # 落櫻側顏
│   ├── cg_stance.jpg        # 拔刀架勢
│   ├── cg_throne.jpg        # 高階紅座
│   └── cg_blade.jpg         # 月夜鏡刃
└── chapters/                # 【純文字創作區】與程式碼完全分開
    ├── manifest.json        # 章節目錄設定檔（控制導航列與首頁卡片順序）
    ├── chapter_01.txt       # 第一節純文字檔
    ├── chapter_02.txt       # 第二節純文字檔
    ├── chapter_03.txt       # 第三節純文字檔
    ├── chapter_04.txt       # 第四節純文字檔
    └── chapter_05.txt       # 第五節純文字檔
```

## ✍️ 未來如何新增「第六節、第七節...」？（完全不用改 HTML）

1. 在 `chapters/` 資料夾裡新增一個純文字檔，例如 `chapter_06.txt`。
   - 第一行寫章節標題，空一行後直接寫正文段落即可。
   - 若要在文章中間插入圖片，只需獨立一行寫：`[CG: images/圖片檔名.jpg | 圖片說明文字]`
   - 若要插入系統提示框，只需獨立一行寫：`[QUOTE: 提示框內容]`
2. 打開 `chapters/manifest.json`，複製一個區塊貼上並修改 `id`、`file`、`title` 等資訊。
3. 將修改後的檔案 Push 到 GitHub，網站就會自動更新！

## 🚀 如何上傳到 GitHub 並免費上線？

1. 登入 [GitHub](https://github.com/)，點擊右上角 `+` -> **New repository**，建立一個新的儲存庫（例如 `nyannyan-shinobi-novel`）。
2. 點擊頁面上的 **uploading an existing file**，將本資料夾內的**所有檔案與資料夾**（`index.html`、`README.md`、`chapters/`、`images/`）直接拖曳進去，點擊 **Commit changes**。
3. **開啟免費網址（二選一）**：
   - **方法 A（GitHub Pages）**：進入儲存庫的 `Settings` -> 左側選單 `Pages` -> `Branch` 選擇 `main` 並按 `Save`，等 1 分鐘即可獲得 `https://你的帳號.github.io/nyannyan-shinobi-novel/` 網址。
   - **方法 B（Netlify 連結 GitHub）**：在 Netlify 點擊 `Add new site` -> `Import an existing project` -> 選擇 GitHub 並綁定此儲存庫，以後只要在 GitHub 更新 `.txt` 文字檔，Netlify 就會自動重新部署！
