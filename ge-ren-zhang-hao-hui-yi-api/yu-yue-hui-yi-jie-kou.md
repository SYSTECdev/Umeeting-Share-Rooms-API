# 1、个人账号预约会议接口

## URL

[https://api.systeccloud.com/umeeting/private/schedule](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| topic | 是 | String | 会议主题 |
| start\_time | 是 | String | 开始时间，格式如：2017-08-19 00:00:00 |
| duration | 是 | Integer | 会议持续时间，以分钟为单位，必须大于30 |
| password | 否 | String |  |
| host\_id | 是 | String | 个人账号所对应hostId |
| mute\_upon\_entry | 否 | String | true:入会时静音，false: 入会时不静音 |
| webinar | 否 | String | "true": 为网络研讨会，“false": 网络会议，默认false |

## 响应

```javascript
{
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "host_key": "030488",         //主持人密钥
        "meeting_id": "1825940376",   //会议号
        "join_url": "",               //入会链接
        "host_id": "8Eki",            //主持人hostId
        "token": "jgkjgkjaae",         //开始会议token
        "ready_time": 15,              // 提前入会时间
        "start_url": ""                // 开始会议的url
    }
}
```

