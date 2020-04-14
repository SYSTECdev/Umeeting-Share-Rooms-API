调整会议方数

---

### URL

[https://api.systeccloud.com](https://api.systeccloud.com/umeeting/share/schedule)/umeeting/livestream/status

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| action | 是 | String | "start"-开始推流，"stop"-结束推流 |
| id | 是 | String | 会议号 |

### 响应

```js
{
    "status" : 200,     // 状态码，200为成功，其他值为失败
    "message" : "OK",   // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : null
}
```



