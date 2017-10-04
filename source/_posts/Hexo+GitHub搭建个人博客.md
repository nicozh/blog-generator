---
title: Hexo+GitHub搭建个人博客
tags: web前端
---


### 搭建步骤
#### .GitHub创建个人仓库
#### .安装Git
#### .安装Node.js
#### .安装Hexo
#### .部署GitHub Pages
#### .发布文章

### GitHub创建个人仓库
登录到GitHub,如果没有GitHub帐号，使用邮箱注册GitHub帐号。点击GitHub中的New repository创建一个新的空仓库，仓库名为：【用户名】.github.io 这个用户名使用你的GitHub帐号名称代替。列如：xxx.github.io
### 安装Git
搭建Git环境，[安 装 Git][1]

### 安装Node.js
搭建Node.js运行环境，[安 装 Node.js][2]
### 安装Hexo
Node环境搭好后，就可以用npm安装Hexo了。

 1. $ npm install -g hexo-cli   // 全局安装hexo-cli
 2. $ hexo init my-blog         // 创建一个hexo框架
 3. $ cd my-blog                // 进入目录
 4. npm install               // 安装依赖包
 5. hexo generate             // 生成静态文件（结果文件）    

hexo框架目录：

|—— _config.yml             // 网站的配置信息
|—— package.json            // 项目包信息 
|—— scaffolds               // 模板文件夹
|—— source                  // 存放用户资源的地方
|   |—— _drafts             // 存放草稿
|   |—— _posts              // 存放文章
|—— themes                  // 主题文件夹

框架常用命令：

 1. $ hexo generate  // 简写：hexo g，生成静态文件，会在当前目录下生成一个public文件夹
 2. $ hexo server       // 简写：hexo s，启动本地服务，用于博客的预览
 3. $ hexo deploy       // 简写：hexo d，部署到远程（如GitHub，可以在_config.yml中配置）
 4. $ hexo new post-name // 简写：hexo n post-name， 新建文章
 5. $ hexo new page page-name   //简写：hexo n page page-name，新建页面
 6. $ hexo d -g                 // 生成和部署
 7. $ hexo s -g                 // 生成和预览

设置主题：

 1. https://github.com/hexojs/hexo/wiki/Themes 上面有主题合集
 2. 随便找一个主题，进入主题的 GitHub 首页，比如我找的是 https://github.com/ppoffice/hexo-theme-hueman
 3. 复制它的 SSH 地址或 HTTPS 地址，假设地址为 git@github.com:ppoffice/hexo-theme-hueman.git
 4. $ git clone  git@github.com:ppoffice/hexo-theme-hueman.git
 5.将my blog目录下的 _config.yml配置文件中的theme属性，设置为hexo-theme-hueman
### 部署GitHub Pages
1. GitHub Pages用于介绍托管在GitHub的项目，每个帐号只能创建一个repository来存放GitHub Pages，而且仓库名称必须是username/username.github.io，这是固定的命名约定。
2. 创建后，可以通过http://username.github.io来访问个人主页。GitHub Pages中个人主页的内容是在master分支下的。部署Hexo到GitHub Pages指的就是将hexo -g 生成的静态文件推送到GitHub Pages对应的仓库中。
3. Hexo提供了hexo-deployer-git工具，可以帮助部署Hexo到很多平台。
4. 执行命令： $ npm install hexo-deployer-git --save
5. 修改_config.yml中的配置：
deploy:
  type: git
  repo: 【填新建的仓库地址】
  branch: master
6.  执行命令：
$ hexo d

### 发布文章

命令行输入：
$ hexo n “博客名字”
我们会发现在my blog根目录下的source文件夹中的_post文件夹中多了一个 博客名字.md 文件，使用Markdown编辑器打开，开始写博客。参考 [Markdown语法][3]
使用命令：
$ hexo g
$hexo d
推送到GitHub pages,然后就可以去http://username.github.io查看博客啦


  [1]: https://git-scm.com/
  [2]: https://nodejs.org/zh-cn/
  [3]: http://wowubuntu.com/markdown/#list