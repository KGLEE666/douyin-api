# douyin-api


**API说明**

* 请求方式没有特殊说明均为`POST`,提交方式`x-www-form-urlencoded`
* 在`headers`中传递`token`  `Authorization:Bearer {token}`
* `{host}`:`......`
* 返回格式统一为：

```
{
   "code": 1,
   "data": [],
   "message": "请求成功"
}
```

参数说明

| 编号 | 参数 | 名称 | 说明 |
| --- | --- | --- | --- |
| 1 | code | 成功标识 | 1：成功，0：失败 |
| 2 | message | 响应信息 |  |
| 3 | data | 返回的数据 |  |


QQ：2697437520