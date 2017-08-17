# 获取会议Token接口

---

### URL

[https://api.systeccloud.com/umeeting/share/token](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secure | 是 | String | API secure |
| meeting\_id | 是 | String | 会议号 |

### 响应

```js
{
    "status" : 200,     // 状态码，200为成功，其他值为失败
    "message" : "OK",   // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "host_id" : "", // 会议主持人账号ID
        "token" : ""    // 会议主持人账号Token
    }
}
```



