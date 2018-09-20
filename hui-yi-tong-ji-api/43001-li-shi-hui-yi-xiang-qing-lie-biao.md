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
            "uuid": "jny6Sttx8NitKXw==",
            "id": 1376669196,
            "host": "test03 ",
            "email": "test03@rfchina.com",
            "user_type": "Corp",
            "start_time": "2018-01-02T03:53:18Z",
            "end_time": "2018-01-02T04:02:10Z",
            "duration": "9分钟",
            "participants": 2,
            "has_pstn": false,
            "has_voip": false,
            "has_3rd_party_audio": false,
            "has_video": false,
            "has_screen_share": false,
            "recording": 0
        },
        {
            "uuid": "kpSi6A4nTMUxctsQ==",
            "id": 1396312207,
            "host": "test03 ",
            "email": "test03@rfchina.com",
            "user_type": "Corp",
            "start_time": "2018-01-02T09:29:47Z",
            "end_time": "2018-01-02T09:31:27Z",
            "duration": "2分钟",
            "participants": 2,
            "has_pstn": false,
            "has_voip": false,
            "has_3rd_party_audio": false,
            "has_video": false,
            "has_screen_share": false,
            "recording": 0
        },
        {
            "uuid": "xqWWWA==",
            "id": 1397639071,
            "host": "test05 ",
            "email": "test05@rfchina.com",
            "user_type": "Corp",
            "start_time": "2018-01-03T02:47:21Z",
            "end_time": "2018-01-03T02:50:32Z",
            "duration": "4分钟",
            "participants": 2,
            "has_pstn": false,
            "has_voip": false,
            "has_3rd_party_audio": false,
            "has_video": false,
            "has_screen_share": false,
            "recording": 0
        }
    }
```



