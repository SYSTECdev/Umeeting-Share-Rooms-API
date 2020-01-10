# 默认获取会议与会者详情（在线，结束的）

---

### URL

[https://api.systeccloud.com/umeeting](https://api.systeccloud.com/umeeting/share/schedule)/metrics/participants

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| uuid | 是 | String | 会议uuid（可以从历史会议列表接口里获取） |
| type | 否 | String | live—在线（默认），past—结束 |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "id": "",
            "user_id": "50342912",
            "user_name": "华润内蒙古医药",
            "device": "iOS",
            "ip_address": "110.16.71.150",
            "cn": "CN",
            "city": "Baotou",
            "network_type": "有线",
            "join_time": "2019-12-20T02:13:18Z",  （UTC格式）
            "leave_time": "2019-12-20T02:28:19Z",  （UTC格式）
            "share_application": false,
            "share_desktop": false,
            "share_whiteboard": false,
            "recording": false
        },
        {
            "id": "",
            "user_id": "50343936",
            "user_name": "河南信息部-陈亚辉",
            "device": "Windows",
            "ip_address": "125.46.15.26",
            "cn": "CN",
            "city": "Zhengzhou",
            "network_type": "有线",
            "join_time": "2019-12-20T02:28:11Z",
            "leave_time": "2019-12-20T02:28:19Z",
            "share_application": false,
            "share_desktop": false,
            "share_whiteboard": false,
            "recording": false
        }
    ]
}
```



