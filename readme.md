

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


## 使用


```

var mdap = require("mdarticleparse")
var fs = require('fs')

var content= fs.readFileSync('file_path',{encoding:'utf8'})

var Obj_out = mdap(content)

```
