# Willem Meng 的个人主页

这是一个纯静态个人主页，页面样式参考 [Kien T. Pham（TK）的个人主页](https://github.com/tkpham3105/tkpham3105.github.io)。页面使用原生 HTML 和 CSS，不需要 Node.js、依赖安装、构建或页面 JavaScript。

## 维护页面

- `index.html`：主页全部内容，包括个人简介、新闻、论文、教育经历、研究兴趣、审稿服务和荣誉。
- `stylesheet.css`：主页样式。页面内容和样式由这两个文件维护。
- `static/assets/img/photo.jpg`：个人照片；`static/assets/favicon.ico`：站点图标。
- `contents/*.md` 和 `contents/config.yml`：旧模板中的原始资料备份，当前主页不会读取这些文件。
- `static/css/` 和 `static/js/`：旧模板资源，当前主页不会加载。

现有页面保留 7 篇论文、9 条新闻、2 段教育经历、6 条荣誉、研究兴趣和审稿服务。原始资料对博士毕业年份分别记为 2025 年和 2026 年 2 月；该日期存在冲突，页面暂时保留来源中的信息。

## 本地预览

可直接在浏览器打开 `index.html`。也可以在仓库根目录启动本地 HTTP 服务：

```bash
python -m http.server 8000
```

然后访问 <http://localhost:8000>。

## 添加论文图片或真实链接

部分论文条目已经加入核验过的正式论文链接。其余论文或代码仓库获得真实 URL 后，可在 `index.html` 中对应论文条目添加链接。图片文件可放入 `static/assets/img/`，并使用相对仓库根目录的路径引用；论文或项目链接应填写可核验的真实 URL。带图片的条目使用 `has-image` 和 `publication-image` class，样式会自动适配桌面端和移动端。

论文链接放在论文信息下方，格式如下：

```html
<div class="publication-links" aria-label="Publication links">
  <a href="https://example.com/paper" target="_blank" rel="noreferrer">[paper]</a>
  <a href="https://github.com/example/project" target="_blank" rel="noreferrer">[code]</a>
</div>
```

## 发布

本仓库适用于 GitHub Pages。将仓库发布为 GitHub Pages 并选择包含 `index.html` 的分支或目录即可；没有构建步骤或生成目录。
