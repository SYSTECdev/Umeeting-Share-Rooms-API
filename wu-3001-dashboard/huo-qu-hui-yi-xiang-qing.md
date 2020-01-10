# 获取会议详情列表（在线，结束）

---

### URL

[https://api.systeccloud.com/umeeting](https://api.systeccloud.com/umeeting/share/meetingTime)/metrics/meetings

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 是 | String | 标准格式时间 "2018-01-01"（注意：查询时段不能超多一个月，超过一个月只能查询出最后一个月时段记录） |
| to | 是 | String | 标准格式时间 “2018-01-01”（注意：查询时段不能超多一个月，超过一个月只能查询出最后一个月时段记录） |
| type | 否 | String | live—在线（默认），past—结束 |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "uuid": "mzejqFKBR/Oz0a46oSvqtg==",
            "id": 1317246759,
            "topic": "工程部_李冬的网络会议",
            "host": "公共会议室 ",
            "email": "umeetingTest1561618892948@systec.com.cn",
            "user_type": "企业用户",
            "start_time": "2019-09-01T00:54:50Z",                           （注意：这里是UTC格式）
            "end_time": "2019-09-01T04:49:58Z",                             （注意：这里是UTC格式）  
            "duration": "03:55:08",
            "participants": 25,
            "has_pstn": false,
            "has_voip": true,
            "has_3rd_party_audio": false,
            "has_video": true,
            "has_screen_share": true,
            "has_recording": true,
            "has_sip": false
        },
        {
            "uuid": "1qEvuDkAROapbbbcNUxEyA==",
            "id": 1550404564,
            "topic": "合约部",
            "host": "公共会议室 ",
            "email": "umeetingTest1561616116190@systec.com.cn",
            "user_type": "企业用户",
            "start_time": "2019-09-02T01:19:38Z",
            "end_time": "2019-09-02T01:21:03Z",
            "duration": "01:25",
            "participants": 2,
            "has_pstn": false,
            "has_voip": true,
            "has_3rd_party_audio": false,
            "has_video": true,
            "has_screen_share": false,
            "has_recording": false,
            "has_sip": false
        }
    ]
}
```



