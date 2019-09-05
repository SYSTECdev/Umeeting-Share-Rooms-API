# \(废弃）会议详情（包括参会人员信息，仅返回进行中或已结束会议信息）

---

### URL

[https://api.systeccloud.com/umeeting/share/meetingdetail](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_id | 是 | String | 会议号 |
| type | 是 | String | 查询类型，1 在线会议，2 历史会议 |
| page\_size | 否 | String | 参会人分页大小 |
| page\_number | 否 | String | 参会人分页页码 |

### 

### 响应

```js
{
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": [
        "data": {
        "uuid": "qHu12qI/==",
        "id": 1390480983,
        "type": "Live Meeting",
        "host": "测试8 ",
        "email": "shareroom18@systec.com.cn",
        "user_type": "Corp",
        "start_time": "2018-08-13T09:46:53Z",
        "end_time": "",
        "duration": null,
        "has_pstn": false,
        "has_voip": true,
        "has_3rd_party_audio": false,
        "has_video": false,
        "has_screen_share": false,
        "recording": 0,
        "participants_count": 1,
        "page_count": 1,
        "page_number": 1,
        "page_size": 100,
        "participants": [
            {
                "id": "",
                "user_id": "16778240",
                "user_name": "叶大红的 iPhone",
                "device": "iOS",
                "ip_address": "183.61.126.78",
                "cn": "CN",
                "city": "Guangzhou",
                "network_type": "Wifi",
                "join_time": "2018-08-13T09:46:53Z",
                "leave_time": ""
            }
        ]
    }
}
```



