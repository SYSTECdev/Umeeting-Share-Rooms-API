# 会议统计报表（每个user\_key对应的会议汇总）

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/meetingTime)userReport

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 是 | String | 标准格式时间 "2018-01-01" |
| to | 是 | String | 标准格式时间 “2018-01-01” |
| user\_keys | 否 | Array | 用户身份自定义信息，用于标识预约会议用户身份，不能超过两百个字节 |

### 响应

```js
    "status": 200,
    "message": "OK",
    "data": [
        {
            "user_key": "123456",                   // 用户user_key
            "total_minutes": 35,                    // 会议时长
            "total_meetings": 9,                    // 会议个数
            "total_participants": 23                // 与会者个数

        },
        {
            "user_key": "123356",                   // 用户user_key
            "total_minutes": 35,                    // 会议时长
            "total_meetings": 9,                    // 会议个数
            "total_participants": 23                // 与会者个数
        }
    }
```



