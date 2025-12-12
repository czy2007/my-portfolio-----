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

在這次作業中使用 `git revert` 回復某個 commit。

**原因：** 進行 A/B 測試時實現了標籤雲版本的技能區（commit `302abd6`），該設計使用 flexbox 和漸層背景展示技能標籤。經過評估，決定回到原始的 CSS Grid 設計，以保持更清晰的網格結構。因此使用 `git revert 302abd6` 回復此提交，並生成了 revert commit `d39c155`。

**為什麼使用 revert 而不是 reset？** git revert 會生成新的 commit 記錄，保留完整的 git 歷史，便於追蹤所有設計決策和實驗過程。

## A/B 版本實驗說明

針對技能區（Skills Section）實施了兩種設計版本的實驗：

### A 版本：標籤雲版 ✓ (採用)
- **分支：** `feature/skills-tags`
- **特色：** 使用 flexbox 包裹、漸層背景（紫藍色）、圓角標籤、hover 放大效果
- **狀態：** 已合併到 main
- **選擇原因：** 設計更現代，視覺層級清晰，互動反饋優良

### B 版本：進度條版 ✗ (未採用)
- **分支：** `feature/skills-bars`
- **特色：** 垂直排列、漸層進度條、標籤名稱與百分比視覺化
- **狀態：** 分支存在但未合併到 main
- **未選擇原因：** 樣式較傳統，與現代 UI 設計趨勢相比不夠突出

## GitHub Pages 部署

網站已啟用 GitHub Pages，使用 main 分支進行部署。

## GitHub Pages 部署

網站已啟用 GitHub Pages，使用 main 分支進行部署。
