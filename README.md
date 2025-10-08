# 实验室网站（Hugo + Wowchemy）

本仓库包含基于 Hugo 与 Wowchemy 的实验室网站骨架，已配置 GitHub Actions 自动部署到 GitHub Pages。

## 本地预览
- 安装 Hugo Extended（0.127+）
- 运行：`hugo server -D`

## 部署到 GitHub Pages
- 将本仓库推送到 GitHub（建议分支 `main`）
- 在仓库 Settings > Pages：
  - Source 选择 `GitHub Actions`
- 推送后触发工作流，完成后通过 Pages 地址访问

## 自定义域名（可选）
- 在域名服务商配置：
  - 顶级域 A 记录指向 GitHub Pages IP：185.199.108.153/109.153/110.153/111.153
  - `www` 子域 CNAME 到 `yourname.github.io.`
- 仓库 Settings > Pages > Custom domain 填写域名，并启用 HTTPS

## 结构说明
- `config/_default/`：站点配置（标题、菜单、参数）
- `content/`：内容目录
  - `home/`：首页模块（Hero/People/Publications）
  - `authors/admin/`：负责人信息
  - `project/`：研究方向/项目
  - `publication/`：论文条目

## 用机构页面完善信息
你提供的机构页面：
- https://gibh.cas.cn/team/gjj/202408/t20240808_7260725.html

建议将该页面中的姓名、职称、简介、研究方向、联系方式等补充进：
- `content/authors/admin/_index.md`
- `content/project/`（为每个方向新增 Markdown 条目）
- `content/publication/`（为代表性论文新增条目，或导入 BibTeX）

如需我继续：
- 我可以按该页面内容补齐负责人信息、研究方向条目，并创建若干代表性论文页面。请确认负责人姓名与偏好展示的研究方向列表。
