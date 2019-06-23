调整会议方数

---

### URL

[https://api.systeccloud.com](https://api.systeccloud.com/umeeting/share/schedule)/umeeting/share/resetCapacity/{meetingId}

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_capacity | 是 | int | 调整方数 |

### 响应

```js
{
    "status" : 200,     // 状态码，200为成功，其他值为失败
    "message" : "OK",   // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : null
}
```



