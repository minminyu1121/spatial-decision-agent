# 語意驅動型空間決策與生成 Agent MVP

單一檔案前端原型，用語意權重（舒服、隱私、遮陰）驅動 100×100 網格上的 A* 尋路，並即時視覺化路徑與 Agent 決策報告。

## 線上使用（分享給別人）

**不必一定要 Vercel。** 這是純靜態網頁，以下兩種都免費：

| 方式 | 適合情境 |
|------|----------|
| **GitHub Pages**（建議） | 程式已在 GitHub，開啟 Pages 即有 `https://你的帳號.github.io/倉庫名/` |
| **Vercel** | 想要一鍵部署、自訂網域、或之後加更多頁面時 |

### GitHub Pages 開啟步驟

1. 打開此 repo 的 **Settings → Pages**
2. **Build and deployment** → Source 選 **Deploy from a branch**
3. Branch 選 `main`，資料夾選 **/ (root)**，儲存
4. 約 1–2 分鐘後可用：`https://minminyu1121.github.io/spatial-decision-agent/`

### 本機使用

1. 用瀏覽器直接開啟 `index.html`（無需安裝、無後端）。
2. 左側選擇語意標籤或拖動滑桿，右側畫布會即時重算路徑。
3. 切換「放置樹木 / 放置圍牆」後點擊畫布可增刪障礙物。

## 技術要點

- 純 HTML + Tailwind CDN + Vanilla JS
- A* 含方向狀態（轉彎懲罰）
- 移動代價：`1 + 舒服×轉彎 + 隱私×遠離圍牆 + 遮陰×曝曬`

## 檔案

- `index.html` — 完整可執行原型
