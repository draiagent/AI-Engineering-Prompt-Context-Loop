# AI 工程四層進化地圖

這是一個可直接部署到 GitHub Pages 的單頁知識網站，用一頁說明：

- 提示詞 Prompt
- 提示詞工程 Prompt Engineering
- 上下文工程 Context Engineering
- Loop 工程 Loop Engineering

## 網站特色

- 繁體中文響應式設計
- 單一 `index.html`，無需安裝套件
- CSS 與 JavaScript 均內嵌，方便維護與搬移
- 四層比較、Agent Loop、失敗模式與能力分級
- 支援桌機、平板與手機
- 可直接使用 GitHub Pages 部署

## 專案結構

```text
AI-Engineering-Prompt-Context-Loop/
├── index.html   # 完整單頁網站
├── README.md    # 專案與部署說明
└── .nojekyll    # 關閉 Jekyll 處理
```

## 本機預覽

最簡單的方式是直接用瀏覽器開啟 `index.html`。

也可以在專案資料夾執行：

```bash
python -m http.server 8000
```

然後開啟：

```text
http://localhost:8000
```

## 上傳到 GitHub

### 方法一：上傳至既有 Repository

1. 在 GitHub 開啟目標 Repository。
2. 選擇 **Add file → Upload files**。
3. 將本資料夾內的三個檔案上傳到 Repository 根目錄。
4. 按下 **Commit changes**。

### 方法二：使用 Git 指令

```bash
git init
git add index.html README.md .nojekyll
git commit -m "feat: add AI engineering one-page guide"
git branch -M main
git remote add origin https://github.com/你的帳號/你的Repository.git
git push -u origin main
```

## 啟用 GitHub Pages

1. 進入 Repository 的 **Settings**。
2. 左側選擇 **Pages**。
3. 在 **Build and deployment** 選擇 **Deploy from a branch**。
4. Branch 選擇 `main`，資料夾選擇 `/(root)`。
5. 按下 **Save**，等待 GitHub 完成部署。

部署網址通常為：

```text
https://你的帳號.github.io/你的Repository/
```

## 自訂內容

- 網站標題：搜尋 `<title>` 與 `<h1>`。
- 主色：修改 CSS `:root` 內的色彩變數。
- 品牌名稱：修改導覽列 `.brand` 與頁尾內容。
- 新增 Logo：在 `.brand` 內以 `<img>` 取代 `.brand-mark`。

## 技術說明

本專案採用原生 HTML、CSS 與少量 JavaScript，不依賴外部框架或 CDN，適合教學展示、企業簡報延伸頁面與 GitHub Pages 靜態部署。
