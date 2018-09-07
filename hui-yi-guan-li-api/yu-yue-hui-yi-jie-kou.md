# 预约会议接口

---

### URL

[https://api.systeccloud.com/umeeting/share/schedule](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| topic | 是 | String | 会议主题 |
| meeting\_capacity | 是 | Integer | 会议方数 |
| start\_time | 是 | String | 开始时间，格式如：2017-08-19 00:00:00 |
| duration | 是 | Integer | 会议持续时间，以分钟为单位，必须大于30 |
| option\_jbh | 否 | String | 允许主持人入会前加入会议，true/false，true为允许，false为不允许 |
| password | 否 | String | 会议密码 |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |

### 响应

```js
{
    "status": 200,                                 //状态码，200为成功，其他值为失败
    "message": "OK",                               // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "host_key": "030488",                      //主持人密钥
        "join_url": "https://**/j/1770498237",     //入会链接
        "meeting_id": "1770498237",                //会议号  
        "start_time": "7",                         //会议开始时间   
        "host_id": "8Eki6-0R7eVsdg-mH4y7A",        //主持人hostId
        "token": "fTlrrST1Ve8iLAMM0NCQXVvaVlTM3M9" //开始会议token
    }
}
```



