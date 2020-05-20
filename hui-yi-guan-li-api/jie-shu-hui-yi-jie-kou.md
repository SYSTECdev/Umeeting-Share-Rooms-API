---
description: （如果会议是周期会议时，id如果传的是会议号则会结束整个周期系列的所有会议，如果传的是周期会议的中某个会议的uuid，则只会结束对应的会议记录）
---

# 5、结束会议接口

## URL

[https://api.systeccloud.com/umeeting/share/end](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| id | 是 | String | 会议号（或者会议uuid） |

## 响应

```javascript
{
    "status" : 200,  // 状态码，200为成功，其他值为失败
    "message" : "OK" // 本次请求结果信息，如果为错误时，即为详细的错误信息
}
```

