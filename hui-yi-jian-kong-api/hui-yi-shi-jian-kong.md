# 1、会议室监控（监控api预约）

## URL

[https://api.systeccloud.com/umeeting/share/rooms](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |

## 响应

```javascript
{
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": [
        {
            "id": "2-Vhs-ODRFS3AvstEXupxQ",       //hostId
            "email": "shareroom3@systec.com.cn",  //会议室账号邮箱
            "first_name": "3",                    //会议室名称
            "meeting_capacity": "25",             //会议室方数
            "meetings": [                         //已预约或者正在进行中的会议
                {
                    "duration": "50",
                    "start_time": "2018-04-26 15:00:00",
                    "host_key": "367260",
                    "topic": "王者荣耀世界大战",
                    "meeting_capacity": "25",
                    "id": "1370845021",
                    "type": "2",
                    "status": "0"
                }
            ]
        }
}
```

