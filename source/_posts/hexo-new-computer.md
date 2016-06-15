---
title: hexo博客托管Github后，在新电脑上同步hexo的方法
date: 2016-06-15 17:48:18
tags: [hexo,github]
categories: 自建博客
---

整体思路是通过其他git分支储存hexo原始文件

## 最初电脑上的设置
1. 参考[hexo官方文档](https://hexo.io/docs/)，构建hexo博客。
2. 在该目录下创建仓库，如[chyin.github.io](http://chyin.github.io)（即使之前创建了仓库，在hexo init后，仓库的信息会被覆盖，仍需要重新建立）。
3. 设置hexo为默认分支（需将博客文件备份在此分支）。
4. 修改_config.yml中的deploy参数，分支应为master。（之前已改的可忽略此布）。
5. 依次执行git add .、git commit -m "..."、git push origin hexo提交网站相关的文件。
6. 执行hexo clean & hexo g & hexo clean & hexo deploy 生成网站并部署到GitHub上。

这样一来，在GitHub上的chyin.github.io仓库就有两个分支，一个hexo分支用来存放博客的原始文件，一个master分支用来存放生成的静态网页。

## 日常使用中的设置
每次修改了配置文件，或者更新了新的博客内容，要先在github上提交本次修改，然后再提交hexo生成发布。此顺序可尽量避免各种意外情况。
## 在新机器上配置hexo，并同步设置
1. 使用git clone git@github.com:chyin/chyin.github.io.git 拷贝仓库.
2. 安装node.js，并在本地新拷贝的chyin.github.io文件夹下通过Git bash依次执行下列指令：npm install -g hexo-cli、npm install、npm install hexo-deployer-git。此时已经不需要hexo init这条指令，如果hexo init会使之前已经克隆下来的 .git消失。

## 参考文档
0. [hexo官方文档](https://hexo.io/docs/)
1. ~~mashiro的hexo构建文档~~ [原地址](https://www.mashiro.io/2015/09/hexo-guide-2/)
1. [Git教程-廖雪峰的官方网站](https://www.baidu.com/link?url=6lILEQjGnfWGlneCMAi3IBA2cZQ7ErVtUvmz9G0Ax2JqRTFg2nZbYvtQfucLE1UWYTmNrDWZxDn-mMsZUKi1WT5f0wYnV5neCLPJXxoAY2n2S4E2kSQLjgY-7wyEJeos&wd=&eqid=ac4259fe000113140000000357600058)
2. [知乎：使用hexo，如果换了电脑怎么更新博客？](https://www.zhihu.com/question/21193762/answer/79109280)