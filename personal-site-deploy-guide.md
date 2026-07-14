# 个人网站交付与部署清单

## 已完成

- 已创建一个零依赖静态个人网站。
- 已包含首页、作品、关于、记录、联系区块。
- 已包含本地图片资产：`assets/hero-studio.jpg`。
- 已添加 Vercel 配置：`vercel.json`。
- 已初始化 Git 仓库，并创建初始提交：`Initial personal website`。

## 本地查看

直接双击项目根目录的 `index.html` 即可打开。

如果你的终端允许监听本地端口，也可以执行：

```bash
python3 -m http.server 3000
```

然后打开：

```text
http://localhost:3000
```

## 上线前替换

在 `index.html` 里替换：

- `你的名字`
- `hello@example.com`
- `https://github.com/yourname`
- 作品标题、作品描述、作品链接
- 最近记录标题与链接

## 推送到 GitHub

在 GitHub 创建一个空仓库后，在项目根目录执行：

```bash
git remote add origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main
```

如果已经添加过远端但地址写错了，使用：

```bash
git remote set-url origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main
```

## 部署到 Vercel

1. 登录 Vercel。
2. 选择 Add New Project / Import Project。
3. 选择刚推送到 GitHub 的仓库。
4. Framework Preset 选择 Other。
5. Build Command 留空。
6. Output Directory 留空。
7. 点击 Deploy。

之后每次推送到 `main` 分支，Vercel 都会自动重新部署。
