# 4、个人账号获取会议信息接口

## URL

[https://api.systeccloud.com/umeeting/private/get](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_id | 是 | String | 会议ID |

## 响应

```javascript
{
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息  
     "data": {
        "duration": "60",             //会议持续时间
        "start_time": "2018-**",      //会议开始时间
        "del_flag": "1",              //删除标记 0 正常 1 已删除
        "password": "",               //入会连接
        "join_url": "",
        "topic": "Topic",              //会议主题
        "id": "1561759092",
        "status": "0"
    }
}
```

