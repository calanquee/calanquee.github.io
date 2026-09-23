# Qingxiu Liu 的学术主页

这是基于 [Academic Pages](https://github.com/academicpages/academicpages.github.io) 的个人学术主页，保留原版侧栏布局、响应式样式和明暗主题切换。

- 网站：<https://calanquee.github.io/>
- 仓库：<https://github.com/calanquee/calanquee.github.io>
- 已填写：Qingxiu Liu；The Chinese University of Hong Kong (CUHK)；Ph.D. Candidate；Computer Systems。
- 栏目：About、Research、Publications、Teaching、CV。

模板中的演示论文、课程、博客、报告、虚构 CV 和评论已清除。研究详情、论文、教学经历和 CV 尚待补充；当前网页明确显示待更新状态。

## 最常编辑的文件

| 文件 | 用途 |
| --- | --- |
| `_config.yml` | 网站标题、侧栏姓名、单位、邮箱、头像与 Scholar 链接 |
| `_pages/about.md` | 首页介绍和教职求职说明 |
| `_pages/research.md` | 研究主题、代表工作与未来方向 |
| `_publications/` | 每篇论文对应一份 Markdown 文件 |
| `_teaching/` | 每门课程或教学经历对应一份 Markdown 文件 |
| `_pages/cv.md` | CV 页面；上传 PDF 后再添加下载链接 |
| `_data/navigation.yml` | 顶部导航顺序 |
| `images/` | 照片和图片；现有 `profile.png` 为通用占位头像 |
| `files/` | 自己的 CV、论文 PDF 或其他附件 |

填写顺序和字段说明见 [CONTENT_GUIDE.md](CONTENT_GUIDE.md)。README、填写指南和维护脚本均已从网站构建中排除。

## 下一步补充

1. 公开邮箱、个人照片、Google Scholar 链接；可按需要补充院系和导师。
2. 两到三条研究主线，以及能说明个人贡献的代表工作。
3. 完整作者列表、论文题目、发表状态、年份与论文/代码链接。
4. 真实的教学、指导、教育、研究经历与学术服务。
5. 最新 CV PDF；确认文件存在后再添加下载链接。

不要将示例、占位符或尚未确认的信息当成正式履历发布。没有资料的可选侧栏字段保持留空，页面不会显示这些链接。

## 本地预览

使用 Ruby **3.3** 和 Bundler。不要使用 macOS 自带的旧 Ruby；安装并切换到 Ruby 3.3 后再运行：

```sh
cd ~/Desktop/website
ruby --version
gem install bundler
bundle install
bundle exec jekyll serve --host 127.0.0.1
```

打开 <http://localhost:4000/>。Jekyll 的预览资源使用 `localhost`，浏览器也使用这个地址。修改 `_config.yml` 后需要重新启动预览服务。

只生成静态页面以检查构建：

```sh
bundle exec jekyll build
```

## GitHub Pages 发布

继续使用现有仓库的 **Settings → Pages → Deploy from a branch → main → /(root)**。在本地预览并确认内容后，将更改提交并推送到 `main`，GitHub Pages 会重新构建网站。这里只准备了主题和内容文件；本地改动不会自动推送。

`url` 已设为 `https://calanquee.github.io`，`baseurl` 留空。`_site/` 是本地构建产物，不需要提交；请勿添加 `.nojekyll`，否则 GitHub Pages 不会执行 Jekyll 构建。

## 模板来源与许可

上游：[academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io)，快照 `3d28cd2`（2026-09-23 获取）。Academic Pages 基于 [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes)。保留了原始 [LICENSE](LICENSE) 和页脚主题归属。
