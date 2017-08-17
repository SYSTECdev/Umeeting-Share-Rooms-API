# 预约会议接口

---

### URL

[https://api.systeccloud.com/umeeting/share/schedule](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secure | 是 | String | API secure |
| topic | 是 | String | 会议主题 |
| meeting\_capacity | 否 | Integer | 会议方数 |
| start\_time | 是 | String | 开始时间，格式如：2017-08-19 00:00:00 |
| duration | 是 | Integer | 会议持续时间，以分钟为单位，必须大于30 |
| password | 否 | String |  |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |

### 响应

```js
{
    "status" : 200, // 状态码，200为成功，其他值为失败
    "message" : "OK", // 状态消息
    "data" : {
        "meeting_id": "15464648254" // 会议号
    }
}
```



