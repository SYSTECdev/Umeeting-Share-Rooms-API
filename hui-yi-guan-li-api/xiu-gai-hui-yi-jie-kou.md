# 修改会议接口

---

### URL

[https://api.systeccloud.com/umeeting/share/update](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| id | 是 | String | 会议号 |
| topic | 否 | String | 会议主题 |
| option\_jbh | 否 | String | 允许主持人入会前加入会议，true/false，true为允许，false为不允许 |
| start\_time | 是 | String | 会议开始时间，yyyy-MM-dd  HH:mm:ss |
| duration | 是 | Integer | 会议持续时间（分钟） |
| password | 否 | String | 会议密码 |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |

### 响应

```js
{
    "status" : 200,  // 状态码，200为成功，其他值为失败
    "message" : "OK" // 本次请求结果信息，如果为错误时，即为详细的错误信息
}
```



