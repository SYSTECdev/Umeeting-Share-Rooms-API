# 会议详情（包括参会人员信息，仅返回进行中或已结束会议信息）

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

### 响应

{

    "status": 200,

    "message": "OK",

    "data": {

        "uuid": "qHu12qI/T0mQMYfBHbPEYg==",

        "id": 1390480983,

        "type": "Live Meeting",

        "host": "测试8 ",

        "email": "shareroom18@systec.com.cn",

        "user\_type": "Corp",

        "start\_time": "2018-08-13T09:46:53Z",

        "end\_time": "",

        "duration": null,

        "has\_pstn": false,

        "has\_voip": true,

        "has\_3rd\_party\_audio": false,

        "has\_video": false,

        "has\_screen\_share": false,

        "recording": 0,

        "participants\_count": 1,

        "page\_count": 1,

        "page\_number": 1,

        "page\_size": 100,

        "participants": \[

            {

                "id": "",

                "user\_id": "16778240",

                "user\_name": "叶大红的 iPhone",

                "device": "iOS",

                "ip\_address": "183.61.126.78",

                "cn": "CN",

                "city": "Guangzhou",

                "network\_type": "Wifi",

                "join\_time": "2018-08-13T09:46:53Z",

                "leave\_time": ""

            }

        \]

    }

}

