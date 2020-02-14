# 获取会议云端录制信息

---

### URL

[https://api.systeccloud.com/](https://api.systeccloud.com/umeeting/share/meetingTime)umeeting/cloud/recording

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| start\_time | 是 | String | 标准格式时间 如“2020-02-02 14:25:12” |
| meeting\_id | 是 | String | 这里可以是会议号，也可以是会议记录的uuid（一场会议里面可能有多条会议记录，每天会议记录都会有唯一的uuid），会议记录需要同步历史会议记录 |

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



