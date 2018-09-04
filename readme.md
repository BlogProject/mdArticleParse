

## 安装

add package.json

```
  "dependencies": {
    "mdarticleparse": "git+https://github.com/BlogProject/mdArticleParse"
  },
```

run cmd in bash

```
npm i 
```

## 文章格式


```

---
#this is yaml header
title: mytitle
tags:
 - tag1
 - tag2
---


# 这里写文章的内容

下面的more之前的内容都是摘要
<!--more-->
如果没有,默认500字内容是摘要

```


## 使用


```javascript
var mdap = require("mdArticleparse")
var Obj_out = mdap(md_file_path)
```

返回的内容为:

如果yaml头
```
{
  content:文章的内容,
  noheader:true
}
```

如果有yaml头
```
{
  content:文章的内容,
  title:这是标题
  time:
  tags:[tag1,tag2]
}
```

## 时间转换的使用

```
var timeTran = require("mdArticleParse/time.js")

console.log(timeTran('2015-10-16 17:01'));
```
