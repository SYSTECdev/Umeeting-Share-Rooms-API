# 公共会议室会议详情接口

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)reports

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| uuid | 是 | String | "uuid":"tIEAQbEIQz6t7rzwAcJ04g==,aZESCNh6Qj2irKauQETyQQ==,Ov8vv4PiR/mYW3Px8NuJVg=="多个会议UUID以”，“隔开 |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "uuid": "xQi0Q/qxQr2iNGdamVfpGg==", //会议uuid
            "id": 1571106323,                    //会议号
            "type": "Past Meeting",              //类型
            "host": "7 ",
            "email": "shareroom7@systec.com.cn", //会议室邮箱
            "user_type": "Corp",                 //host类型
            "start_time": "2018-05-08T02:32:34Z", //开始时间 需要自己转换为标准时间
            "end_time": "2018-05-08T02:37:38Z",   //结束时间 需要自己转换为标准时间
            "duration": "6分钟",                  //持续时间
            "has_pstn": false,
            "has_voip": true,
            "has_3rd_party_audio": false,
            "has_video": true,
            "has_screen_share": false,
            "recording": 0,
            "participants_count": 3,               //参会人数
            "page_count": 1,
            "page_number": 1,
            "page_size": 100,
            "participants": [                     //参会人信息
                {
                    "id": "zn_VfIR-TG-IaZgdU1chmg",
                    "user_id": "16778240",
                    "user_name": "systec",
                    "device": "Windows",
                    "ip_address": "116.31.75.13",
                    "cn": "CN",
                    "city": "Guangzhou",
                    "network_type": "Wired",
                    "join_time": "2018-05-08T02:32:34Z",
                    "leave_time": "2018-05-08T02:37:38Z"
                },
                {
                    "id": "",
                    "user_id": "16779264",
                    "user_name": "叶大红的 iPhone",
                    "device": "iOS",
                    "ip_address": "116.31.75.13",
                    "cn": "CN",
                    "city": "Guangzhou",
                    "network_type": "Wifi",
                    "join_time": "2018-05-08T02:34:06Z",
                    "leave_time": "2018-05-08T02:35:50Z"
                },
                {
                    "id": "95azRXz1QaCzH66_UqJptg",
                    "user_id": "16780288",
                    "user_name": "测试账号",
                    "device": "iOS",
                    "ip_address": "116.31.75.13",
                    "cn": "CN",
                    "city": "Guangzhou",
                    "network_type": "Wifi",
                    "join_time": "2018-05-08T02:37:09Z",
                    "leave_time": "2018-05-08T02:37:29Z"
                }
            ]
        },
        {
            "id": "1579334441"    //只有已结束并且至少有两个参会人的会议才有报表，否者只返回会议ID 
        },
        {
            "id": "1897462468"
        },
        {
            "id": "1565208463"
        },
        {
            "id": "1304637394"
        }
    ]
}
```



