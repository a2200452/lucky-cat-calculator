# 招財貓的理財筆記｜買房 vs 股息試算

純靜態網站（3 個檔案），用 GitHub Pages 免費上線，全程 0 元。

## 一、上線（約 5 分鐘）
1. 登入 github.com，右上角 + → **New repository**
   - Repository name：`lucky-cat-calculator`（想要最短網址可取名 `你的帳號.github.io`）
   - 選 **Public**（免費帳號的 GitHub Pages 需要公開 repo）
   - 勾 **Add a README file** 不用勾，直接 Create
2. 進入 repo → **Add file → Upload files**，把 `index.html`、`config.js`、`README.md` 一起拖進去 → **Commit changes**
3. **Settings → Pages**：Source 選 **Deploy from a branch**，Branch 選 `main`、資料夾 `/ (root)` → **Save**
4. 等 1–2 分鐘，頁面上方會出現網址：`https://你的帳號.github.io/lucky-cat-calculator/`（或 `https://你的帳號.github.io/`）

## 二、開啟數據追蹤（全部免費，兩個可擇一或都用）
只需要編輯 `config.js`（在 GitHub 點檔案 → 鉛筆圖示 → 貼上 → Commit）。

**A. Cloudflare Web Analytics（看流量、來源、裝置；免 cookie）**
1. cloudflare.com 免費註冊 → Analytics & Logs → **Web Analytics** → **Add a site**
2. Hostname 填 `你的帳號.github.io` → 複製 token
3. 貼進 `config.js` 的 `CF_TOKEN: '這裡'`

**B. Google Analytics 4（看按鈕與行為）**
1. analytics.google.com 建立資源 → 資料串流 → 網站，網址填你的 github.io 網址
2. 複製 `G-` 開頭的衡量 ID，貼進 `GA_ID: '這裡'`
3. 事件會自動送出（約 24 小時後出現在報表）：

| 事件名稱 | 意思 |
|---|---|
| `calculate_click` | 按了「更新試算結果」 |
| `edit_input`（field） | 第一次改了哪個欄位 |
| `calc_result`（winner、years） | 停止輸入後的結果：etf / house / tie |
| `toggle_advanced` | 展開或收合進階設定 |
| `reset` | 按了重設 |
| `dm_click` | 點「聊聊我的方案」→ 進 IG 私訊（最重要的轉換） |
| `ig_profile_click` | 點「追蹤更多理財小筆記」 |

建議到 GA4 → 管理 → 事件，把 `dm_click` 標成 **關鍵事件**，就能直接看到導流到私訊的人數。

## 三、隱私
- 不會傳送任何輸入的金額，只記錄「有沒有操作、哪邊勝出、點了哪個按鈕」
- 瀏覽器開啟「不要追蹤」時，完全不載入統計
- 兩個設定都留空 = 完全不追蹤

## 四、之後更新
直接在 GitHub 重新上傳同名檔案覆蓋，1–2 分鐘後網站就會更新，網址不變。
