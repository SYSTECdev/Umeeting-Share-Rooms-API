# 8、获取会议与会者

## URL

[https://api.systeccloud.com/umeeting](https://api.systeccloud.com/umeeting/share/schedule)/public/meeting/{meetingId}/participants

\*\*\*\*

## **参**数

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
    "data": {
        "duration": "180",
        "start_time": "2020-03-25 11:30:00",
        "total_minutes": 967,
        "total_participants": 19,
        "topic": "雄县业务部_郭福庆的网络会议",
        "id": "1300133319",
        "participants_list": [
            {
                "user_id": "16778240",
                "user_name": "鲁文涛",
                "device": "Windows",
                "ip_address": "182.51.86.221",
                "location": "Hebei (CN)",
                "network_type": "Wifi",
                "join_time": "2020-03-25 11:28:24",
                "leave_time": "2020-03-25 12:20:56",
                "share_application": false,
                "share_desktop": false,
                "share_whiteboard": false,
                "recording": false,
                "pc_name": "",
                "domain": "",
                "mac_addr": "",
                "harddisk_id": "",
                "version": "4.3.47204.0325",
                "leave_reason": ""
            }
        ]
    }
}
```

