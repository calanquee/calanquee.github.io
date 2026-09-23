# 主页内容填写指南

本文件仅供维护主页，不会生成公开网页。已确认的信息是 Qingxiu Liu、CUHK、Ph.D. Candidate 和 Computer Systems；其余资料按下面顺序补充即可。

## 1. 侧栏与联系方式

修改 `_config.yml` 的 `author` 部分：

- `email`：你愿意公开的学术邮箱。
- `googlescholar`：你自己的完整 Google Scholar 个人主页地址。
- `avatar`：将照片放到 `images/`，这里写文件名，例如 `portrait.jpg`。目前使用通用灰色占位头像。
- `location`、`pronouns`、`orcid`：可选；不需要时保持留空。
- `employer`：已填 `CUHK`，可在确认后补充院系。

YAML 使用空格缩进，不要用 Tab；包含冒号的文字加引号。暂不填写的字段保持冒号后为空，不要填假的邮箱或 `#` 链接。

## 2. 首页与研究

`_pages/about.md` 已包含身份、Computer Systems 研究方向和寻找教职的说明。可以补充：

- 当前具体研究问题，以及为什么它值得解决。
- 你个人的关键贡献。
- 未来独立开展研究的方向。
- 确认后的求职时间与可入职时间。

`_pages/research.md` 适合组织两到三条研究主线，每条用一个标题和一小段说明，再链接到对应论文、代码或项目。

现有页面中的 `<!-- ... -->` 是编辑提示，不会显示在正常页面上；更新正文后可删除。

## 3. 论文

每篇论文在 `_publications/` 中创建一个 Markdown 文件，例如按真实发表日期命名为 `YYYY-MM-DD-short-title.md`。空目录中的 `.gitkeep` 不会显示为论文。

文件最上方用两行 `---` 包住 YAML 元数据：

| 字段 | 填写内容 |
| --- | --- |
| `title` | 真实论文题目，使用引号 |
| `collection` | `publications` |
| `permalink` | 唯一地址，例如 `/publication/short-title/` |
| `date` | 真实日期，格式 `YYYY-MM-DD` |
| `venue` | 实际发表会议或期刊 |
| `excerpt` | 一到两句贡献介绍，可包含完整作者列表 |
| `paperurl` | 可访问的论文 URL；没有就省略 |
| `citation` | 完整作者、题目、会议/期刊和年份 |

第二个 `---` 后写论文简介、代码链接或其他补充材料。添加后会自动出现在 Publications 页面，按日期倒序排列。

当前原版模板对论文条目使用 “Published in” 文案，适用于已发表论文。添加预印本或已接收但未发表的工作时，需先调整展示文案并明确标注状态，不能用已发表标签代替。不要给待发表工作编造发表日期。

上传自己的附件到 `files/` 后可用 `/files/文件名.pdf` 链接；只添加实际存在的文件或可访问的网址。

## 4. 教学与指导

`_teaching/` 的每个 Markdown 文件对应一项真实经历。元数据可使用 `title`、`collection: teaching`、`type`、`venue`、`date`、`permalink` 和 `excerpt`。`type` 明确写 Instructor、Teaching Assistant 或实际职责，`venue` 写学校与课程所属单位。正文说明教学内容和你的具体工作。

没有相关经历时保留待更新提示，或从 `_data/navigation.yml` 暂时移除 Teaching。只移除导航不会删除页面本身。

## 5. CV

上传最新 PDF 为 `files/cv.pdf`，然后在 `_pages/cv.md` 增加：

```markdown
[Download CV (PDF)]({{ '/files/cv.pdf' | relative_url }})
```

确认 PDF 文件存在后再添加链接。CV 页面还可以填写教育、研究工作、教学、奖励及学术服务；日期、角色和成果均以真实资料为准。当前没有默认 CV 下载按钮，因此不会指向不存在的附件。

## 6. 发布前检查

- 用真实资料替换对应的 “coming soon” 提示。
- 检查姓名、单位、论文作者、发表状态和日期。
- 点击所有邮箱、Scholar、论文、代码与 CV 链接。
- 在手机宽度以及亮色、暗色模式下浏览。
- 运行 `bundle exec jekyll build`，确认没有构建错误。

完成后提交并推送到 `main`；现有 GitHub Pages 的 `main / (root)` 发布设置会构建网站。
