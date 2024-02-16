+++
title = 'hugo使用'
date = 2024-02-16T19:21:07+08:00
draft = false
+++
#### 克隆博客源仓库
```bash
git clone https://github.com/xxxxxx/blogs.git
```

#### 安装主题
```bash
cd hugo-blog
git submodule add https://github.com/alex-shpak/hugo-book.git themes/hugo-book
vim hugo.toml
把theme=的内容改为主题名
theme = 'hugo-book'
```
#### 生成静态后进入public,推送到xxx.github.io
```bash
cd public
git init -b main
git remote add origin git@github.com:xxx/xxx.github.io.git
git pull --rebase origin main
git add .
git commit -m "说明“
git push -f origin main
```
#### 推送博客源仓库
```bash
cd ../../
git add .
git commit -m '说明'
git push
```

参考[如何用 GitHub Pages + Hugo 搭建个人博客](https://cuttontail.blog/blog/create-a-wesite-using-github-pages-and-hugo/)