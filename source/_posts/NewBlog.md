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
{% timeline %}
{% timenode 2019.Previous %}
使用过Emlog Wordpress来搭建博客，使用过各种博客系统。
{% endtimenode %}
{% timenode 2019 %}
尝试在CSDN 简书平台发布自己的文章，但不太喜欢，遂转入Typecho
{% endtimenode %}
{% timenode 2020 %}
typecho小而美的感觉是很不错的体验加上我正好会使用PHP，所以能自己搓插件。
{% endtimenode %}
{% timenode 2021 %}
域名备案和准备高考，搭建了一个运行在国内的博客。
{% endtimenode %}
{% timenode The first half of 2022  %}
没有空闲时间打理博客，备案丢失，意外将电脑中typecho的备份删除故跑路
{% endtimenode %}
{% timenode The second half of 2022  %}
依靠Hexo搭建了全新的博客，不折腾了。
{% endtimenode %}
{% endtimeline %}

各位好啊，我又新搭了Hexo博客，以上就是悲剧经历了。

之前我一直使用typecho，服务器和域名在国内备案，高中学业繁忙，每天都忙着学习。
所以个人就没有时间处理相关的事情😭，导致国内备案掉了，加上本来博文写的就不怎么样，
后来干脆就直接删掉跑路了。

直到2022年的下半年毕业，我终于想起时修理博客，却又嫌折腾博客麻烦，国内备案审核挺烦。
本来是计划在某大佬那里使用Typecho搭建博客，typecho某些地方有些实在是难受，

于是我决定博客使用hexo搭建，并且以低成本实现搭个稳定的博客，博客是是非常适合移动，轻松可以在新的地方使用。

## 博客搭建
[博客源码-Github](https://github.com/MliKiowa/MliKiowa.github.io)

本博客通过使用GithubAction等方式生成部署分发博文到如githubpage vercel等服务商
至于推送到`cos/oss .etc storage bucket`还是算了，毕竟谁用谁欠费(容易挨打 好点情况也得宕了)

(本博客使用多服务商同时也涉及到Dns分流 腾讯的这种解析要交钱升级才能支持 所以域名估计在国外一家dns解析)
### 小吐槽
居然`github action`只有已经写好的`deploy hugo site to githubpage workflow`，没有hexo自动部署的，还得我改了半天(水平有限)。
这么大个github没人发布这种吗?(还是不能发布，~~总之本懒人强烈谴责这种行为~~。
快给我整个方便脚本(~~bushi~~)对了，如果有需求可以直接Clone删掉博文 稍加修改也可使用 仅仅需要修改几行代码即可运行
### 博客基于?
{% table %}
| Name | Content |
| -------- | -------- |
| Blog | Hexo |
| Theme | volantis |
| platform | vercel |
| domain | nanaeo.cn |
{% endtable %}

之前还想试试`hexo-theme-diaspora`这样的主题(移植wp到hexo的，看介绍图很好看)，可惜作者没更新了，不更新了，于是我只能选择其它主题了。
所以我换成了volantis主题 (`npm -i hexo-theme-volantis` 可以轻松安装)，个人感觉色调和布局都很好看，可玩程度很高。

## 迁移使用
通过以下脚本可以快速迁移，从云端下载源码然后在本地进行编写博文。

{% folding bash.sh %}
```
git clone https://github.com/MliKiowa/MliKiowa.github.io
cd xxx
npm install
hexo g
```
{% endfolding %}
## 博客内容
1. Dev Exp.
2. Site Log.
3. Life.
## 期盼
1. ~~原来的域名气质好憨(被我朋友有幸嘲笑)~~，怎么能配得上新博客。
所以我还是注册个符合气质的新域名啊，现在选好了是nanaeo.cn
好看吧。
2. 折腾数次`emlog wp typecho hugo`真的是太累了，所以本博客能run起来我觉得不是不会去折腾什么新博客了，我还是努力成为年更博主吧。
细节的话等我慢慢完善吧。

