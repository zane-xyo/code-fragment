
- 精确搜索，需要使用双引号引起来
```elasticsearch
path:"/app/logs/nginx/access.log"
```


- 模糊搜索
```elasticsearch
path:"/app/~"
```

- 匹配0到多个字符
```elasticsearch
*oken
```

- 匹配单个字符
```elasticsearch
tok?n
```

- +：搜索结果中必须包含此项 -：不能含有此项 什么都没有则可有可无
```elasticsearch
+token -appVersion appCode
```


- 运算符AND/OR/NOT必须大写
```elasticsearch
token AND uid ；token OR uid；NOT uid
```

- 允许一个字段值在某个区间（[] 包含该值，{}不包含）
```elasticsearch
@version:[1 TO 3]
```

- 组合查询
```elasticsearch
(uid OR token) AND version
```

- 转义特殊字符 + – && || ! ( ) { } [ ] ^ ” ~ * ? : \ 转义特殊字符只需在字符前加上符号\
