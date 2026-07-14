# 个人网站

这是一个零依赖静态个人网站，可以直接部署到 GitHub + Vercel。

## 本地预览

```bash
python3 -m http.server 3000
```

然后打开 `http://localhost:3000`。

## 替换成你的信息

- 在 `index.html` 里搜索 `你的名字`，替换成真实姓名或昵称。
- 把 `hello@example.com` 改成你的邮箱。
- 把 `https://github.com/yourname` 改成你的 GitHub 地址。
- 修改“近期项目”和“最近记录”里的标题、描述与链接。
- 如果你想换首屏图片，替换 `assets/hero-studio.jpg`，文件名保持不变即可。

## 推送到 GitHub

1. 在 GitHub 新建一个空仓库，不要勾选自动创建 README。
2. 本项目已经完成 `git init` 和初始提交；你只需要添加远端并推送：

```bash
git remote add origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main
```

如果你以后从零重建，可以使用：

```bash
git init
git add .
git commit -m "Initial personal website"
git branch -M main
```

GitHub 官方文档也提供了通过命令行创建仓库、添加远端并推送的流程；如果你习惯 GitHub CLI，也可以用 `gh repo create`。

## 部署到 Vercel

1. 登录 Vercel。
2. 选择 Add New Project / Import Project。
3. 选择刚推送到 GitHub 的仓库。
4. Framework Preset 选择 Other，Build Command 留空，Output Directory 留空。
5. 点击 Deploy。

Vercel 会连接 GitHub 仓库；之后每次推送到 `main` 分支，都会自动触发一次新的部署。
