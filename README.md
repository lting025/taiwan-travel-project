# 島嶼慢遊 Taiwan Travel Notes

以台灣觀光景點為主題的靜態網站，示範如何利用 `AGENTS.md` 制定一致的內容與開發規則，讓 AI 後續擴充景點。範例包含駁二藝術特區、蓮池潭和日月潭水社碼頭，提供搜尋、地區篩選與景點詳情。

## 在電腦瀏覽
不需安裝套件，在專案資料夾執行：

```bash
python3 -m http.server 8000 -d dist
```

瀏覽器開啟 http://localhost:8000/。也可以直接開啟 `dist/index.html`。

## 請 AI 新增景點
將整個專案交給 AI，輸入：「請先閱讀 AGENTS.md，依照規則新增台南安平古堡，查證官方資料，並檢查搜尋與地區篩選。」新增資料後會自動生成卡片，不需要重新設計網站。

## 上傳 GitHub 並部署 GitHub Pages
1. 在 GitHub 建立新的公開儲存庫，將本專案完整內容上傳，包含 `.github` 資料夾。
2. 在儲存庫 **Settings → Pages → Build and deployment** 中選擇 **GitHub Actions**。
3. `.github/workflows/pages.yml` 會在推送至 `main` 時部署 `dist/`；如預設分支不是 `main`，請修改 workflow。
4. 在 **Actions** 確認部署成功，再到 Pages 取得公開網址；網址由你的帳號與儲存庫名稱決定。

景點的開放狀況、交通及票價可能更動，請以官方最新公告為準。
