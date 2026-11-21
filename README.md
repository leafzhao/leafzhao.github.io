# leafzhao.github.io — 学术主页

基于 [al-folio](https://github.com/alshedivat/al-folio)（Jekyll）的学术个人主页，部署在 <https://leafzhao.github.io/>。
生活博客在另一个仓库：[leafzhao/astro-blog](https://github.com/leafzhao/astro-blog)（<https://leafzhao.github.io/astro-blog/>）。

## 常改的文件

| 想改什么 | 文件 |
| --- | --- |
| 首页简介、照片、右侧信息 | `_pages/about.md`（照片放 `assets/img/prof_pic.jpg`，再把 `profile.image` 设为 `prof_pic.jpg`） |
| 论文列表 | `_bibliography/papers.bib`（加 `selected = {true}` 的会显示在首页） |
| 期刊缩写徽章颜色 | `_data/venues.yml` |
| 简历（CV 页） | `_data/cv.yml`（教育、工作经历已留好注释模板，取消注释后填写） |
| 社交链接（Scholar、GitHub、ORCID、邮箱…） | `_data/socials.yml` |
| 站点名称、描述、功能开关 | `_config.yml` |
| Google Scholar 引用数徽章 | `_data/citations.yml` |

论文数据最初从 Google Scholar（user=FBvFs0cAAAAJ）抓取，并用 Crossref 补全了完整作者、DOI 和页码；
会议报告和个别没有 DOI 的条目作者不完整（以 `others` 结尾），可手动补全。

## 本地预览

```bash
bundle install
LANG=C.UTF-8 bundle exec jekyll serve   # http://localhost:4000/
```

## 部署

推送到 `main` 后，`.github/workflows/deploy.yml` 自动构建并发布到 GitHub Pages
（仓库 Settings → Pages → Source 需选 **GitHub Actions**）。

更多定制说明见 `docs/`（来自 al-folio 上游）。
