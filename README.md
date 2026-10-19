# 谈典 · 机械工程简历 / 作品集

纯静态站点，无构建步骤，直接打开 `index.html` 即可预览。

## 结构

```
index.html                 简历主页（在原站基础上扩展）
portfolio/index.html       作品集（板块式，按文件夹划分）
assets/art/*.webp          美术作品图（800px 大图 + 420px 缩略图）
assets/docs/*              工程项目文档（PDF / XLSX）
```

## 相对原站的改动

1. 顶栏新增「作品集 PORTFOLIO」按钮（紫青渐变 + 扫光动效）
2. 侧栏目录下方新增「作品集」玻璃卡片入口
3. 新增 `portfolio/` 子页，按 `美术项目` / `工程项目` 两个文件夹划分板块
   - 美术：9 件神兽，点击开灯箱（键盘 ←/→ 翻页、ESC 关闭、移动端左右滑动）
   - 工程：3 份文档（程序 PDF 在线预览、BOM / I/O 表格下载）
4. 修正原 `.toc a` 选择器会误吞新增入口的问题，统一改为 `#toc a`

## 部署（GitHub Pages）

```bash
git init && git add . && git commit -m "resume + portfolio"
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
# Settings → Pages → Branch: main / root
```
