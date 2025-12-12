# My Portfolio

此專案為個人簡歷單頁網站範例，包含以下區塊：

- Header / 導航
- 關於我（About）
- 技能（Skills） — 使用 CSS Grid 排列標籤並加上 hover 放大效果
- 經歷（Experience）
- 作品集（Portfolio）
- 聯絡（Contact）

## 檔案說明

- `index.html` — 網站主頁
- `styles.css` — 樣式（包含 Grid 與響應式規則）
- `script.js` — 互動腳本

## 本地預覽

在專案根目錄啟動簡易 HTTP 伺服器（需要 Python）：

```bash
python -m http.server 8000
# 然後在瀏覽器開啟 http://localhost:8000/index.html
```

## 實作重點

- 技能區使用 `.skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); }`，在窄螢幕（<=600px）時改為單欄。
- `.skill-tag` 加上 `transition` 與 `:hover { transform: scale(1.06) }` 來達成 hover 放大效果。

## Git 工作流

- **main** — 正式版本，標籤雲版技能區
- **feature/skills-tags** — 標籤雲版實驗（已合併）
- **feature/skills-bars** — 進度條版實驗（未合併）

## 版本回復紀錄

在這次作業中使用 `git revert` 回復某個 commit。原因是：進行 A/B 測試時，需要測試不同的技能區實現方式（進度條 vs 標籤雲），先嘗試進度條版本，但後來決定採用標籤雲版，因此回復了進度條版本的提交，以保持 git 歷史的清晰和可追蹤性。具體 revert 的 commit 是用於測試進度條的實驗性修改。

## GitHub Pages 部署

網站已啟用 GitHub Pages，使用 main 分支進行部署。
