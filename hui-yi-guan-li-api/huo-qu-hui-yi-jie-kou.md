# 获取会议接口

---

### URL

[https://api.systeccloud.com/umeeting/share/get](https://api.systeccloud.com/umeeting/share/get)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_id | 是 | String | 会议ID |

### 响应

```js
{
    "status" : 200,                           // 状态码，200为成功，其他值为失败
    "message" : "OK",                         // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "duration" : 20,                      // 会议持续时间  
        "start_time" : "2017-08-15 00:00:00", // 会议开始时间
        "topic" : "HelloWorld!",              // 会议主题
        "id" : "1360671085",                  // 会议号
        "status" : 1                          // 会议状态，0-已预约，1-进行中
        "meeting_capacity" : 10,              // 会议方数
        "password" : "",                      // 会议密码
        "user_key" : ""                       // 用户
    }
}
```



