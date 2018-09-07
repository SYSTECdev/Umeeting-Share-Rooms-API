# 即时会议接口（会议开始30分钟后，如果系统检测到该会议没有参会者人进入，系统将删除该会议，释放会议室资源）

---

### URL

[https://api.systeccloud.com/umeeting/share/instant](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| topic | 是 | String | 会议主题 |
| option\_jbh | 否 | String | 允许主持人入会前加入会议，true/false，true为允许，false为不允许 |
| meeting\_capacity | 是 | Integer | 会议方数 |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |
| duration | 否 | Integer | 会议持续时间，以分钟为单位，必须大于30 |

### 响应

```js
{
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "host_key": "873380",         //主持人密钥
        "meeting_id" : "15464648254", // 会议号
        "host_id" : "",               // 主持人账号ID，由SDK调用
        "token" : ""                  // 主持人账号Token，有SDK调用
    }
}
{
    "status": 200,                                 // 状态码，200为成功，其他值为失败
    "message": "OK",                               // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "host_key": "765418",                      //主持人密钥
        "join_url": "https://**/j/1591620888",     //入会链接
        "meeting_id": "1591620888",                // 会议号
        "start_time": "",                          // 开始时间
        "host_id": "mueyYP0sQp-",                  //主持人hostId
        "token": "9AYkPEIrxUzZmU2ZWIQXVvaVlTM3M9"  //开会token
    }
}
```



