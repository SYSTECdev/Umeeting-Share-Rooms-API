# 历史会议详情接口（同一会议号多次开会，会有多条记录）

---

### URL

[https://api.systeccloud.com/umeeting/share/hisMeetin](https://api.systeccloud.com/umeeting/share/meetingTime)g

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 是 | String | 标准格式时间 "2018-01-01"（注意：查询时段不能超多一个月，超过一个月只能查询出最后一个月时段记录） |
| to | 是 | String | 标准格式时间 “2018-01-01”（注意：查询时段不能超多一个月，超过一个月只能查询出最后一个月时段记录） |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "uuid": "hVew/yBeQamdZXVVQBvNhQ==",
            "id": 1525647127,
            "host": "富力 ",
            "email": "test19@rfchina.com",
            "user_type": "Corp",
            "start_time": "2018-04-01 05:33:22",
            "end_time": "2018-04-01 08:18:45",
            "duration": 166,
            "participants": 3,
            "has_pstn": false,
            "has_voip": false,
            "has_3rd_party_audio": false,
            "has_video": false,
            "has_screen_share": false,
            "recording": 0
        },
        {
            "uuid": "tIEAQbEIQz6t7rzwAcJ04g==",
            "id": 1526598269,
            "host": "富力 ",
            "email": "test70@rfchina.com",
            "user_type": "Corp",
            "start_time": "2018-04-02 00:40:24",
            "end_time": "2018-04-02 06:02:36",
            "duration": 323,
            "participants": 12,
            "has_pstn": false,
            "has_voip": false,
            "has_3rd_party_audio": false,
            "has_video": false,
            "has_screen_share": false,
            "recording": 0
        }
    }
```



