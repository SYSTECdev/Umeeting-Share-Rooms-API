# 获取会议与会者QOS（在线，结束的）

---

### URL

[https://api.systeccloud.com/umeeting](https://api.systeccloud.com/umeeting/share/schedule)/metrics/participants/qos

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| uuid | 是 | String | 会议uuid（可以会议详情列表接口里获取） |
| type | 否 | String | live—在线（默认），past—结束 |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "user_id": "16778240",
            "user_name": "扬州万象汇推广部徐伟",
            "device": "Windows",
            "ip_address": "58.220.110.106",
            "location": "Nanjing (CN)",
            "network_type": "Wifi",
            "join_time": "2020-01-10T01:09:02Z",                                     （注意这里是UTC格式）
            "leave_time": "2020-01-10T01:52:26Z",                                    （注意这里是UTC格式）
            "share_application": false,
            "share_desktop": false,
            "share_whiteboard": false,
            "recording": false,
            "pc_name": "",
            "domain": "",
            "mac_addr": "",
            "harddisk_id": "",
            "version": "4.3.47204.0325"
        },
        {
            "user_id": "16788480",
            "user_name": "POLYCOM RMX 2000A",
            "device": "H.323/SIP",
            "ip_address": "218.13.52.59",
            "location": "Guangzhou (CN)",
            "network_type": "其他",
            "join_time": "2020-01-10T01:55:01Z",
            "share_application": false,
            "share_desktop": false,
            "share_whiteboard": false,
            "recording": false,
            "pc_name": "",
            "domain": "",
            "mac_addr": "",
            "harddisk_id": "",
            "version": "4.1.4814.1203|H323"
        }
    ]
}
```



