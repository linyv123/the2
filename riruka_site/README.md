# 管緒リルカ｜音源&角色完整使用规约

UTAU 声库「管緒リルカ」的官网规约页面。单页静态站点，内置 中文 / English / 日本語 三语切换，右上角可下载音源包。

## 站点文件

| 文件 | 说明 |
|---|---|
| `index.html` | 页面本体（三语内容内嵌，无外部依赖） |
| `icon.png` | 角色头像（由音源包 icon.bmp 转换） |
| `管緒リルカ.zip` | 音源包原文件（a.wav / character.txt / oto.ini / icon.bmp / readme.txt） |
| `.nojekyll` | 避免 GitHub Pages 跳过非下划线开头的 Jekyll 处理 |

## 部署到 GitHub Pages（3 步）

1. **新建仓库**：在 GitHub 上创建新仓库，例如 `riruka-voicebank`（公开或私有均可，Pages 公开仓库免费托管）。

2. **推送文件**，把本目录内容作为仓库根目录：
   ```bash
   cd 本目录
   git init
   git add .
   git commit -m "init: 管緒リルカ voicebank terms page"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/<仓库名>.git
   git push -u origin main
   ```

3. **开启 Pages**：仓库 → Settings → Pages → Source 选择 `Deploy from a branch` → 分支选 `main` / 根目录 `/(root)` → Save。等待 1~2 分钟，站点即出现在 `https://<你的用户名>.github.io/<仓库名>/`。

> 提示：如果本机已登录 GitHub CLI（`gh auth login`），可改用：
> ```bash
> gh repo create <仓库名> --public --source . --push
> ```

## 本地预览

直接双击打开 `index.html`，或用任意静态服务器：

```bash
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

下载按钮使用 `download` 属性触发浏览器直接保存 `管緒リルカ.zip`。
