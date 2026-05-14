# ForOutdoor

ForOutdoor 是一个专注户外装备评测、户外运动入门指南、徒步登山滑雪露营装备选购建议的内容站点。内容覆盖冲锋衣、帐篷、睡袋、登山鞋、滑雪装备等品类。

## 部署到 GitHub Pages（推荐，免费）

1. 在 GitHub 注册账号（如果还没有）
2. 创建一个新仓库，名字建议 `forOutdoor` 或 `foroutdoor`
3. 在仓库根目录上传本文件夹所有内容（不包括本 README 也行）
4. 仓库 Settings → Pages → Source 选 main 分支根目录 → Save
5. 几分钟后访问 `https://你的用户名.github.io/仓库名` 即可看到网站
6. 把这个 URL 填到京东联盟"网站管理"提交审核

详细命令行操作：
```bash
cd forOutdoor_site
git init
git add .
git commit -m "init"
git branch -M main
git remote add origin https://github.com/你的用户名/forOutdoor.git
git push -u origin main
```

## 部署到 Gitee Pages（国内访问稳定）

1. gitee.com 注册并实名认证
2. 创建仓库，上传同样的内容
3. 仓库 → 服务 → Gitee Pages → 启动
4. 注意：Gitee Pages 服务需要部署后手动激活，每次更新代码也要重新部署

## 部署到 Vercel / Netlify（最简单）

直接拖文件夹到 vercel.com 或 netlify.com 的"new site"页面即可，10 秒完成。

## 修改与扩展

- 改首页文案：build_site.py 顶部 `SITE_NAME` `SITE_DESC` 等变量
- 加文章：build_site.py 中 `ARTICLES` 列表新增字典即可，重跑脚本
- 改样式：`CSS` 字符串
- 已经部署后想更新内容：改 build_site.py，重跑生成新 HTML，git push 即可

## 文件结构

```
forOutdoor_site/
├── index.html              首页
├── about.html              关于
├── contact.html            联系
├── 404.html                错误页
├── robots.txt
├── sitemap.xml
├── README.md
├── articles/
│   └── *.html (11 篇文章)
├── categories/
│   └── *.html (4 个分类)
└── css/
    └── style.css
```

## 提交京东联盟时填写参考

- 网站名称：ForOutdoor
- 网站 URL：你的 GitHub Pages 实际 URL
- 网站类型：内容资讯 / 评测博客
- 推广类目：户外装备 / 运动户外
- 简介：填 SITE_DESC 那段文字
