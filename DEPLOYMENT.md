# GitHub Pages 部署指南

本專案已準備好在 GitHub Pages 上部署。以下是部署步驟：

## 步驟 1：在 GitHub 建立新倉庫

1. 訪問 [GitHub](https://github.com)，登入帳戶
2. 點擊右上角 **+** → **New repository**
3. 填入倉庫名稱（建議：`my-portfolio` 或 `[username].github.io`）
4. 選擇 **Public**（以啟用 GitHub Pages）
5. 不要初始化 README、.gitignore 或 license
6. 點擊 **Create repository**

## 步驟 2：連接本地倉庫到 GitHub

執行以下命令（將 `username` 和 `repo` 替換為您的 GitHub 用戶名和倉庫名）：

```bash
cd my-portfolio
git remote add origin https://github.com/username/repo.git
git branch -M main
git push -u origin main
```

## 步驟 3：推送所有分支

```bash
# 推送 feature/skills-tags 分支
git push origin feature/skills-tags

# 推送 feature/skills-bars 分支
git push origin feature/skills-bars
```

## 步驟 4：啟用 GitHub Pages

1. 在 GitHub 倉庫頁面，點擊 **Settings**
2. 在左側菜單找到 **Pages**
3. 在 **Source** 下拉選單選擇 **main** 分支
4. 點擊 **Save**
5. 稍等片刻，GitHub 會提供部署的 URL

## 部署完成

部署完成後，網站將在以下 URL 可用：

- 如果倉庫名稱為 `my-portfolio`：
  `https://username.github.io/my-portfolio`

- 如果倉庫名稱為 `[username].github.io`：
  `https://[username].github.io`

## 驗證部署

訪問上述 URL，您應能看到您的個人簡歷網站正常運作，包含所有功能：
- 導航功能正常
- 技能區使用標籤雲設計（tag cloud）
- hover 效果生效
- 響應式設計在手機上顯示為單欄

## GitHub 提交歷史

倉庫包含以下重要提交：

- **feat: add HTML structure...** — 初始 HTML 架構
- **style: add responsive CSS Grid...** — CSS 樣式與響應式設計
- **feat: add form handling...** — JavaScript 互動功能
- **feat: implement tag cloud design...** — 標籤雲版本實驗（已合併）
- **Revert "feat: implement tag cloud design..."** — git revert 演示
- **docs: add git revert and A/B testing explanation...** — 文檔更新

## 分支狀態

- **main** — 正式版本，已部署到 GitHub Pages
- **feature/skills-tags** — 標籤雲設計（已合併到 main）
- **feature/skills-bars** — 進度條設計（未合併，作為實驗版本保留）
