---
layout: post
title: "使用jekyll在github上搭建静态博客"
description: ""
category: 
tags: yunwei
---

##安装本地jekyll
安装jekyll老报失败 

``` python
[houjinchao@mx jekyll]$> sudo gem install jekyll 15-05-14 21:20 
Password: 
ERROR: Could not find a valid gem ‘jekyll’ (>= 0), here is why: 
Unable to download data from https://rubygems.org/ - Errno::ECONNRESET: Connection reset by peer - SSL_connect (https://rubygems.org/quick/Marshal.4.8/jekyll-2.5.3.gemspec.rz) 
ERROR: Possible alternatives: jekyll
```

更换淘宝源后恢复，命令如下：

```python
$ gem sources --remove https://rubygems.org/
$ gem sources -a https://ruby.taobao.org/
$ sudo gem update --system
$ sudo gem install jekyll
```

##安装模板，默认的模板是Maruku，我们替换为RDiscount

``` python
Maruku是纯ruby写的Markdown模板解释器。 RDiscount是C写的模板解释器。
```

##导入jekyll模板
``` python
$ git clone https://github.com/plusjade/jekyll-bootstrap.git
```
