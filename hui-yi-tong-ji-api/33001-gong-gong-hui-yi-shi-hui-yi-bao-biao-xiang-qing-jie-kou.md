# 4、会议详细信息接口（包括参会人）

## URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)meetingdetail

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| uuid | 是 | String | "uuid":"tIEAQbEIQz6t7rzwAcJ04g==,aZESCNh6Qj2irKauQETyQQ==,Ov8vv4PiR/mYW3Px8NuJVg==" 多个会议UUID以 ”，“ 隔开 |

## 响应

```javascript
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
                    "leave_time": "2018-08-13 17:30:22", //离开会议时间
                    "meeting_id": 1371517030,
                    "name": "杨雪鑫",
                    "meeting_uuid": "4XoNt04WQkWm5OAAAX2cQg==",
                    "join_time": "2018-08-13 16:18:41"  //加入会议时间
                },

                {
                    "leave_time": "2018-08-13 17:19:45",
                    "meeting_id": 1371517030,
                    "name": "詹杨信一",
                    "meeting_uuid": "4XoNt04WQkWm5OAAAX2cQg==",
                    "join_time": "2018-08-13 16:35:41"
                },
                {
                    "leave_time": "2018-08-13 17:29:26",
                    "meeting_id": 1371517030,
                    "name": "蔡琼",
                    "meeting_uuid": "4XoNt04WQkWm5OAAAX2cQg==",
                    "join_time": "2018-08-13 16:55:51"
                }
            ]
        }
    ]
}
```

