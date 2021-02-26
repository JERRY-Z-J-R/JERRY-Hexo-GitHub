# JERRY-Hexo-GitHub

**《JERRY Hexo & GitHub 静态网站搭建说明》**

> 原创内容，转载请注明出处！

**目录**

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [JERRY-Hexo-GitHub](#jerry-hexo-github)
- [一、前言](#%E4%B8%80%E5%89%8D%E8%A8%80)
  - [1.1 什么是 Hexo?](#11-%E4%BB%80%E4%B9%88%E6%98%AF-hexo)
  - [1.2 什么是 GitHub?](#12-%E4%BB%80%E4%B9%88%E6%98%AF-github)
  - [1.3 什么是静态网站?](#13-%E4%BB%80%E4%B9%88%E6%98%AF%E9%9D%99%E6%80%81%E7%BD%91%E7%AB%99)
  - [1.4 Hexo 与 GitHub 搭配建站的优缺点](#14-hexo-%E4%B8%8E-github-%E6%90%AD%E9%85%8D%E5%BB%BA%E7%AB%99%E7%9A%84%E4%BC%98%E7%BC%BA%E7%82%B9)
- [二、安装 Git](#%E4%BA%8C%E5%AE%89%E8%A3%85-git)
  - [2.1 什么是 Git？](#21-%E4%BB%80%E4%B9%88%E6%98%AF-git)
  - [2.2 Git 的下载安装与配置](#22-git-%E7%9A%84%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE)
- [三、安装 Node.js](#%E4%B8%89%E5%AE%89%E8%A3%85-nodejs)
  - [3.1 什么是 Node.js?](#31-%E4%BB%80%E4%B9%88%E6%98%AF-nodejs)
  - [3.2 Node.js 的下载安装与配置](#32-nodejs-%E7%9A%84%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE)
- [四、安装 Hexo](#%E5%9B%9B%E5%AE%89%E8%A3%85-hexo)
  - [4.1 Hexo 的下载安装与配置](#41-hexo-%E7%9A%84%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE)
- [五、搭建静态网站](#%E4%BA%94%E6%90%AD%E5%BB%BA%E9%9D%99%E6%80%81%E7%BD%91%E7%AB%99)
  - [5.1 新建一个网站](#51-%E6%96%B0%E5%BB%BA%E4%B8%80%E4%B8%AA%E7%BD%91%E7%AB%99)
  - [5.2 生成静态文件](#52-%E7%94%9F%E6%88%90%E9%9D%99%E6%80%81%E6%96%87%E4%BB%B6)
  - [5.3 启动服务器](#53-%E5%90%AF%E5%8A%A8%E6%9C%8D%E5%8A%A1%E5%99%A8)
  - [5.4 新建一篇文章](#54-%E6%96%B0%E5%BB%BA%E4%B8%80%E7%AF%87%E6%96%87%E7%AB%A0)
- [六、利用 GitHub 部署网站](#%E5%85%AD%E5%88%A9%E7%94%A8-github-%E9%83%A8%E7%BD%B2%E7%BD%91%E7%AB%99)
  - [6.1 注册用户](#61-%E6%B3%A8%E5%86%8C%E7%94%A8%E6%88%B7)
  - [6.2 创建同名仓库](#62-%E5%88%9B%E5%BB%BA%E5%90%8C%E5%90%8D%E4%BB%93%E5%BA%93)
  - [6.3 更改 Hexo 配置文件](#63-%E6%9B%B4%E6%94%B9-hexo-%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)
  - [6.4 安装 hexo - git 部署工具](#64-%E5%AE%89%E8%A3%85-hexo---git-%E9%83%A8%E7%BD%B2%E5%B7%A5%E5%85%B7)
  - [6.5 远程部署到 GitHub Pages 服务器](#65-%E8%BF%9C%E7%A8%8B%E9%83%A8%E7%BD%B2%E5%88%B0-github-pages-%E6%9C%8D%E5%8A%A1%E5%99%A8)
- [七、结束语](#%E4%B8%83%E7%BB%93%E6%9D%9F%E8%AF%AD)
  - [7.1 美化 Hexo 网站](#71-%E7%BE%8E%E5%8C%96-hexo-%E7%BD%91%E7%AB%99)
  - [7.2 使用 Hexo 插件](#72-%E4%BD%BF%E7%94%A8-hexo-%E6%8F%92%E4%BB%B6)
  - [7.3 帮助文档](#73-%E5%B8%AE%E5%8A%A9%E6%96%87%E6%A1%A3)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# 一、前言

## 1.1 什么是 Hexo？

**一个基于 `Node.js` 设计的快速、简洁且高效的博客框架**

- 超快速度
- 支持 Markdown
- 一键部署
- 插件和可扩展性
- 免费开源

## 1.2 什么是 GitHub？

**一个面向开源及私有软件项目的托管平台，因为只支持 `Git` 作为唯一的版本库格式，故名 GitHub**

- 全球最活跃开源社区
- 开源社交平台
- 企业项目管理平台

## 1.3 什么是静态网站？

**通俗的讲静态网站指：只有 `前端` 没有 `后端` 的网站，静态网站的所有页面内容在没有被修改的前提下都是固定不变的**

适用于博客、固定页面展示等网站。

## 1.4 Hexo 与 GitHub 搭配建站的优缺点

**（1）优点**

- 简单稳定
- 开源免费
- 社区活跃利于交流

**（2）缺点：**

- 国内访问速度慢
- 不支持动态网站搭建

# 二、安装 Git

## 2.1 什么是 Git？

**`Git` 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目**

使用 GitHub 必须有 Git。

## 2.2 Git 的下载安装与配置

**（1）下载安装**

[Git官网](https://git-scm.com/)

选择对应系统版本下载，安装默认下一步即可。

**（2）配置**

打开终端键入以下命令：

```bash
$ git --version

# 查看 git 版本号
# 若成功识别即为 git 安装成功
```

```bash
$ git config --global user.name "xxx"
$ git config --global user.email xxx@xxx.com

# 配置个人的用户名称和电子邮件地址
```

```bash
$ git config --list

# ...
# user.name=xxx
# user.email=xxx@xxx.com

## 检查已有的配置信息
# 若配置信息中出现正确用户名及邮箱即为配置成功
```

# 三、安装 Node.js

## 3.1 什么是 Node.js？

一个基于 `Chrome V8` 引擎的 `JavaScript` 运行环境，使用了一个事件驱动 、非阻塞式 I/O 模型，让 JavaScript 运行在服务端的开发平台，它让 JavaScript 成为与 `PHP`、`Python`、`Perl`、`Ruby` 等服务端语言平起平坐的 `脚本语言`。

## 3.2 Node.js 的下载安装与配置

[Node.js官网](https://nodejs.org/zh-cn/)

选择对应系统的长期支持版下载，安装默认下一步即可。

安装完成，打开终端键入以下命令：

```bash
$ node -v

# 查看 Node.js 版本
```

```bash
$ npm -v

# 查看 npm 包管理器版本
```

若以上两个命令都成功识别，那么 Node.js 便安装成功。

```bash
$ npm install -g cnpm --registry=https://registry.npm.taobao.org

# 利用 npm 下载国内淘宝镜像 cnpm
```

```bash
$ cnpm -v

# 查看 cnpm 版本
# 若以上命令成功识别，那么 cnpm 便安装成功
```

**什么是 npm 和 cnpm ?**

- `npm` (node package manager)：Node.js 的包管理器，用于 node 插件管理（包括安装、卸载、管理依赖等）。

- `cnpm`：因为 npm 安装插件是从国外服务器下载，受网络的影响比较大，可能会出现异常，所以乐于分享的淘宝团队解决了这事。来自官网：“这是一个完整 npmjs.org 镜像，你可以用此代替官方版本(只读)，同步频率目前为 10分钟 一次以保证尽量与官方服务同步”。

# 四、安装 Hexo

## 4.1 Hexo 的下载安装与配置

**下载安装：**

[可以参考Hexo官网](https://hexo.io/zh-cn/)

打开终端键入以下命令：

```bash
$ cnpm install hexo-cli -g

# 等待一会，安装完毕
```

```bash
$ hexo -v

# 查看 hexo 版本
# 若以上命令成功识别，那么 hexo 便安装成功
```

# 五、搭建静态网站

## 5.1 新建一个网站

```bash
$ hexo init [folder]

# 如果没有设置 folder，Hexo 默认在当前的文件夹建立网站
```

## 5.2 生成静态文件

```bash
$ hexo generate

# 该命令可以简写为 $ hexo g
```

## 5.3 启动服务器

```bash
$ hexo server

# 该命令可以简写为 $ hexo s
# 默认情况下，访问端口为：http://localhost:4000/
# 在浏览器中访问 http://localhost:4000/ 即可打开本地搭建好的网站
```

## 5.4 新建一篇文章

```bash
$ hexo new <title>

# 如果标题包含空格的话，请使用引号括起来 $ hexo new "first blog"
# 生成的 Markdown 文章放在 source 内的 _posts 下
```

# 六、利用 GitHub 部署网站

## 6.1 注册用户

[GitHub官网](https://github.com/)

点击右上角注册即可。

## 6.2 创建同名仓库

- 点击右上的 `+`，选择 `New repository` 新建一个仓库

- 仓库名称设为 `用户名.github.io`

- 仓库类型为 `Public` 公共类型

- 复制仓库 `HTTPS` URL

## 6.3 更改 Hexo 配置文件

修改根目录 `_config.yml` 内的 `deploy`。

```yml
# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: 'git'
  repo: https://github.com/用户名/用户名.github.io.git	# HTTPS URL
  branch: master
```

## 6.4 安装 hexo - git 部署工具

在 Hexo 博客根目录下，打开终端键入：

```bash
$ cnpm install hexo-deployer-git --save

# 安装 hexo-deployer-git 工具
```

## 6.5 远程部署到 GitHub Pages 服务器

```bash
$ hexo deploy

# 该命令可以简写为 $ hexo d
```

部署成功后即使用 `https://用户名.github.io/` 在浏览器中访问网站。

# 七、结束语

## 7.1 美化 Hexo 网站

Hexo 支持主题自定义，并且有一个活跃的 [主题社区](https://hexo.io/themes/)。

切换主题方法：下载主题到 `themes` 文件夹内并修改根目录 `_config.yml` 内的 `theme` 设定，即可切换主题。

修改配置主题请查阅相应主题的文档。

目前比较热门的几个主题：

- [NexT GitHub](https://github.com/iissnan/hexo-theme-next) 
- [Butterfly GitHub](https://github.com/jerryc127/hexo-theme-butterfly)
- [Yilia GitHub](https://github.com/litten/hexo-theme-yilia)
- [Matery GitHub](https://github.com/blinkfox/hexo-theme-matery)

## 7.2 使用 Hexo 插件

Hexo 是一个支持插件的可扩展框架，具体插件类型及安装方法请前往 [Hexo 官网查看](https://hexo.io/plugins/) 或者 搜索引擎求助。

## 7.3 帮助文档

Hexo 提供了全面的 Hexo [使用文档](https://hexo.io/docs/index.html)（有中文版）及 [API 文档](https://hexo.io/api/)，在使用及开发优化 Hexo 的过程中，建议以官方文档为基准。