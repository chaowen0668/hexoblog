title: hexo使用手册  
categories: 博客

---

以下是我使用hexo的一些历程，搭建过程也挺纠结。网上的很多教程也有些是过时了。综合多方面的参考资料，才写下来这个教程。
<!--more-->
# Hexo的安装 #
## 安装软件与配置 ##
1. 安装git 下载地址 git-scm.com/downloads
2. 安装note.js 下载地址 https://nodejs.org  
   注意:需要添加Path环境变量，使npm命令生效  
`;C:\Program Files\nodejs\node_modules\npm`
## 注册github账号与创建Resposity ##
### 注册账号 ###
忽略
### 创建Resposity ###
创建的时候注意Repository的名字。比如我的Github账号是chaowen0668，那么我应该创建的Repository的名字是：chaowen0668.github.io。注意要勾选生成README文件  
![](http://i.imgur.com/IKynifC.png)
## 安装npm与插件 ##
### 把创建的Repository克隆到本地 ###
### 安装npm ###
    npm install -g hexo 
    hexo init
    npm install
### 本地查看 ###
执行以下命令，然后运行localhost:4000浏览  

    hexo generate
    hexo server
### 安装插件 ###
    npm install hexo-generator-index --save
    npm install hexo-generator-archive --save
    npm install hexo-generator-category --save
    npm install hexo-generator-tag --save
    npm install hexo-server --save
    npm install hexo-deployer-git --save
    npm install hexo-deployer-heroku --save
    npm install hexo-deployer-rsync --save
    npm install hexo-deployer-openshift --save
    npm install hexo-renderer-marked@0.2 --save
    npm install hexo-renderer-stylus@0.2 --save
    npm install hexo-generator-feed@1 --save
    npm install hexo-generator-sitemap@1 --save
## 修改配置文件_config.yml ##
     
    deploy:
      type: git
      repository: https://github.com/chaowen0668/chaowen0668.github.io.git
      branch: master

## 配置ssh ##

# hexo的优化 #
## 主页文章显示摘要 ##
编辑md文件的时候，在要作为摘要的文字后面添加<!--more-->即可.
## 创建分类页面 ##
添加一个 分类 页面，并在菜单中显示页面链接。  

1. 新建一个页面，命名为 categories 。命令如下：  
   `hexo new page categories`
2. 编辑刚新建的页面，将页面的类型设置为 categories ，主题将自动为这个页面显示所有分类.  
    `type: "categories"`  

   注意：如果有启用多说 或者 Disqus 评论，默认页面也会带有评论。需要关闭的话，请添加字段 comments 并将值设置为 false，如：  
  
    title: 分类  
    date: 2014-12-22 12:39:04  
    type: "categories"  
	comments: false
3.在菜单中添加链接。编辑主题的 _config.yml ，将 menu 中的   `categories: /categories` 注释去掉，如下:

	    menu:
    	home: /
    	categories: /categories
    	archives: /archives
    	tags: /tags
## 设置侧边栏头像 ##
编辑站点的 _config.yml，新增字段 avatar， 值设置成头像的链接地址。
其中，头像的链接地址可以是：  
1. 完整的互联网 URL，例如：  
	`http://test.com1.z0.glb.clouddn.com/avatar.jpg`

2.站点内的地址，例如：  

- `/uploads/avatar.jpg` 需要将你的头像图片放置在 站点的 `source/uploads/`（可能需要新建uploads目录）  
- `/images/avatar.jpg` 需要将你的头像图片放置在 主题的 `source/images/` 目录下。

## 创建关于页面 ##
新建一个 about 页面：  
	`hexo new page "about"`  

菜单显示 about 链接，在主题的 _configy.yml 设置中将 menu 中 about 前面的注释去掉即可。

	  menu:
      home: /
      archives: /archives
      tags: /tags
      about: /about

## 设置多说评论 ##
添加 多说 或者 Disqus 第三方评论系统。当同时设置了 多说 和 Disqus 时，优先选择多说。  

1. 使用多说前需要先在 多说 创建一个站点。具体步骤如下：  
 
  - 登录后在首页选择 “我要安装”。
  - 创建站点，填写站点相关信息。注意，多说域名 这一栏填写的即是你的`duoshuo_shortname`

1. 编辑站点的` _config.yml` 注意，不是主题的`_config.yml`文件 ，添加 `duoshuo_shortname` 字段，设置如下

	`duoshuo_shortname: your-duoshuo-shortname`  

（注）duoshuo short name: 你的多说二级域名去掉 .duoshuo.com 部分

## 绑定域名 ##
1. 修改你的域名提供商上的DNS解析，我用了DNSPOD
   域名DNS修改帮助 https://support.dnspod.cn/Kb/guide/  

1. DNSPod上设置github的ip
   github的两个ip地址是`192.30.252.153` 和`192.30.252.154`  
然后在DNSPod设置域名，如下  
![](http://i.imgur.com/2X1EUsV.png)  
1. 在hexo博客设置CNAME  
在博客源文件`./source`下创建一个文件名是`CNAME`的文本文件，该文件内容只有一行，就是你注册的域名。  
如 `94ifeng.com`
 
    







 
  
