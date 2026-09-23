# Holo Card — GitHub Pages

这是一个可直接部署到 GitHub Pages 的静态 Holo Card 项目。

## 项目结构

```text
.
├── index.html
├── .nojekyll
├── assets/
│   ├── background.png
│   ├── character.png
│   ├── structure.png
│   └── ui.png
└── README.md
```

## 方式一：GitHub 网页上传

1. 在 GitHub 新建一个 **Public repository**。
2. 将本目录中的全部文件上传到仓库根目录。
3. 打开仓库：
   **Settings → Pages**
4. 在 **Build and deployment** 中选择：
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
5. 保存后等待 GitHub Pages 发布。
6. 页面地址通常为：

```text
https://你的用户名.github.io/仓库名/
```

## 方式二：Git 命令行

```bash
git init
git add .
git commit -m "Add Holo Card"
git branch -M main
git remote add origin https://github.com/你的用户名/你的仓库名.git
git push -u origin main
```

然后在 GitHub 的 **Settings → Pages** 开启 Pages。

## 注意

- 这是纯静态网页，不需要 Node.js、Python 或服务器。
- `index.html` 必须位于 GitHub Pages 发布目录的根目录。
- `assets/` 必须和 `index.html` 一起上传。
- 页面默认状态为 0° / 0°，各图层与静态正面严格对齐。
- 拖动、倾斜或调整 Depth 后才会产生视差。
- 卡片支持正反面翻转。
- 如果后续修改图片，请保持各图层相同的 1606×2048 画布坐标。

## 生成二维码

GitHub Pages 成功发布后，把最终的 `https://...github.io/.../` 地址发给我，
我可以根据这个网址生成适合手机扫码的高清二维码。
