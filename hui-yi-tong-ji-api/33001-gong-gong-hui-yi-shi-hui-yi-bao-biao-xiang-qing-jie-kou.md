# 公共会议室会议详情接口

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)reports

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_ids | 是 | String | "1571106323,1579334441“多个会议ID以”，“隔开 |

### 响应

```js
{
    "status" : 200,   // 状态码，200为成功，其他值为失败
    "message" : "OK", // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "from" : "2017-8-31", 
        "to" : "2017-09-01", 
        "total_record" : 1, 
        "total_page" : 1, 
        "page_number" : 1, 
        "page_size" : 30, 
        "has_previous_page" : false,
        "has_next_page" : false,
        "meetings" : [
            {
                "uuid" : "dgvOvqWVRUWjrEOS2YI2ig==",           // 会议记录ID
                "host_id" : "ABCDEFGHIJKLMNOPQRSTUVWXYZ",      // 公共会议室ID
                "meeting_id" : "1790001234",                   // 会议号
                "topic" : "Hello world!",                      // 会议主题
                "start_time" : "2017-08-31 00:00:00",          // 会议开始时间
                "duration" : 120,                              // 即时会议、预约会议的持续时间
                "end_time" : "2017-08-31 01:00:00",            // 会议结束时间（即会议被删除的时间）
                "is_extra" : 0,                                // 是否额外会议室，即无可用会议资源时临时生成的会议室
                "participants" : [                             // 该会议的参会者信息
                    {
                        "name" : "XYZ",                        // 参会者显示名称
                        "join_time" : "2017-08-31 00:51:00",   // 参会者加入会议时间
                        "leave_time" : "2017-08-31 00:53:04"   // 参会者离开会议时间
                    }
                ], 
                "telephony_usage" : [                          // 该会议的电话参会者信息
                    {
                        "phone_number" : "+8613716819201",     // 电话号码
                        "type" : "call-out",                   // 呼叫类型
                        "start_time" : "2017-08-31 00:51:00",  // 通话开始时间
                        "end_time" : "2017-08-31 00:53:00",    // 通话结束时间
                        "duration" : 2                         // 通话持续时间
                        "total" : 0.12                         // 通话费用，单位元
                    }
                ]
            }
        ]
    }
}
```



