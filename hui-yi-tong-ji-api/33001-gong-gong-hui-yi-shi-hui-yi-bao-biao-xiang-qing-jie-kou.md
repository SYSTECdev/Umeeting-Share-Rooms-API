# 会议详细信息接口（包括参会人）

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)meetingdetail

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| uuid | 是 | String | "uuid":"tIEAQbEIQz6t7rzwAcJ04g==,aZESCNh6Qj2irKauQETyQQ==,Ov8vv4PiR/mYW3Px8NuJVg==" 多个会议UUID以 ”，“ 隔开 |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "duration": "45",                          //会议持续时间 分钟  
            "start_time": "2018-04-02 10:32:33",       //会议开始时间
            "participants_count": 3,                   //参会人数
            "total_participants_deration": 127,        //参会人数总时长
            "host": "富力",                             //会议室名称 
            "end_time": "2018-04-02 11:17:04",         //结束时间
            "id": "1806697677",                        //会议ID
            "uuid": "Ov8vv4PiR/mYW3Px8NuJVg==",        //会议uuid
            "email": "test67@rfchina.com",
            "participants": [
                {
                    "uuid": "3f5a47d1-718e-4ce8-a20a-d22368a24310", 
                    "meetingId": "1806697677",
                    "name": "Taiyuan-rf",
                    "joinTime": "2018-04-02 10:32:33",       //参会人入会时间
                    "leaveTime": "2018-04-02 11:16:49",      //参会人离开时间
                    "meetingUuid": "Ov8vv4PiR/mYW3Px8NuJVg=="
                },
                {
                    "uuid": "464d5b0d-31a7-4d66-bd71-8fef73f75b59",
                    "meetingId": "1806697677",
                    "name": "hohhot",
                    "joinTime": "2018-04-02 10:32:36",
                    "leaveTime": "2018-04-02 11:17:01",
                    "meetingUuid": "Ov8vv4PiR/mYW3Px8NuJVg=="
                },
                {
                    "uuid": "feb5901a-43cd-4e8c-96ad-051f76bd9cd6",
                    "meetingId": "1806697677",
                    "name": "Administrator",
                    "joinTime": "2018-04-02 10:38:07",
                    "leaveTime": "2018-04-02 11:17:03",
                    "meetingUuid": "Ov8vv4PiR/mYW3Px8NuJVg=="
                }
            ]
        }
    ]
}
```



