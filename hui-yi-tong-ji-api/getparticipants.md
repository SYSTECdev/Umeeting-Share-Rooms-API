# 8、获取会议与会者

## URL

[https://api.systeccloud.com/umeeting](https://api.systeccloud.com/umeeting/share/schedule)/meeting/{meetingId}/participants



## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| topic | 是 | String | 会议主题 |
| host\_id | 是 | String | 用户id（预约会议时返回的） |



```javascript
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "id": "yLiCrj0PSeqexAAputSCFA",  
            "user_id": "16778240",
            "user_name": "王家生",
            "device": "安卓",
            "ip_address": "125.33.25.190",
            "location": "Beijing (CN)",
            "network_type": "Wifi",
            "join_time": "2020-03-05 13:05:37",
            "leave_time": "2020-03-05 14:00:38",
            "share_application": false,
            "share_desktop": false,
            "share_whiteboard": false,
            "recording": false,
            "pc_name": "",
            "domain": "",
            "mac_addr": "",
            "harddisk_id": "",
            "version": "4.3.53571.0118",
            "leave_reason": ""
        }
    ]
}
```

