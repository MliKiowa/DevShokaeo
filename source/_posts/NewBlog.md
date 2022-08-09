---
title: 新博客建好啦
date: 2022-08-05
categories:
    - SiteLog
tags:
    - SiteLog
    - HexoThemes
    - Hexo
---

是全新的依赖于Hexo+vlolantis搭建的博客!

<!-- more -->

## 起因
各位好啊，我又新搭了Hexo博客，具体原因说来复杂。
之前我一直使用typecho，服务器和域名在国内备案，高中学业繁忙，每天都忙着学习，
所以个人就没有时间处理相关的事情😭，导致国内备案掉了，加上本来博文写的就不怎么样，
后来干脆就直接删掉跑路了，直到2022年的下半年毕业，我终于想起时修理博客，却又嫌折腾博客麻烦，国内备案审核也麻烦。
本来是计划在某大佬那里使用Typecho搭建博客，typecho某些地方有些实在是难受，
于是我决定博客使用hexo搭建，并且以低成本实现搭个稳定的博客，博客是是非常适合移动，轻松可以在新的地方使用。
## 搭建
> 博客源码(Github):https://github.com/MliKiowa/MliKiowa.github.io/

本博客通过使用GithubAction等方式生成部署分发博文到如githubpage vercel等服务商
至于推送到Cos/Oss等storage bucket还是算了，毕竟谁用谁欠费(容易挨打 好点情况也得宕了)
(使用多服务商同时也涉及到Dns分流 腾讯的这种解析要交钱升级才能支持 所以域名估计在国外一家dns解析)
### 小吐槽
居然github action只有已经写好的deploy hugo site to githubpage的workflow，没有hexo的，还得我改了半天(水平有限)
,这么大个github没人发布这种吗?(还是不能发布，总之本懒人强烈谴责这种行为，快给我整个方便脚本)对了，如果有需求可以直接Clone删掉博文 稍加修改也可使用 仅仅需要修改几行代码即可运行
### 主题
之前还想试试hexo-theme-diaspora这样的主题(移植wp到hexo的，看介绍图很好看)，可惜作者没更新了，
所以我换成了volantis主题 (npm -i hexo-theme-volantis 可以轻松安装)，个人感觉色调和布局都很好看
## 迁移使用
```script
bash.sh
git clone https://github.com/MliKiowa/MliKiowa.github.io
npm install
hexo g
```
可以很快的到新机器上使用 靠谱
## 展望
原来的域名气质好憨(被我朋友有幸嘲笑)，怎么能配地上新博客，而且还是在腾讯云上注册的，所以讲我还是注册个符合气质的新域名啊
具体是什么域名还得让我考虑考虑，肯定还得好看的(但是我没钱)
折腾数次emlog wp typecho hugo真的是太累了，所以本博客能run起来我觉得不是不会去折腾什么新博客了，我还是努力成为年更博主吧。
细节的话等我慢慢完善吧

