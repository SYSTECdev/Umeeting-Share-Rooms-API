# 公共会议室明细统计接口

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)summary

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 否 | String | 统计起始时间，默认为当天\(查询时间不能超过一个月\) |
| to | 否 | String | 统计结束时间，默认为当天（查询时间不能超过一个月） |
| host\_id | 否 | String | 公共会议室ID，如果没有指定，则查询所有公共会议室的明细信息 |
| page\_size | 否 | Integer | 分页显示，每页大小，不指定时为30 |
| page\_number | 否 | Integer | 分页显示，第几页，不指定时为1 |

### 响应

```js
{
    "status" : 200,   // 状态码，200为成功，其他值为失败
    "message" : "OK", // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "from" : "2017-8-31", 
        "to" : "2017-09-01", 
        "total_record" : 1, 
        "total_page" : 1, 
        "page_number" : 1, 
        "page_size" : 30, 
        "has_previous_page" : false,    
        "has_next_page" : false,
        "total_meetings": 7, //总会议数量
        "total_participants": 17, //总参会人
        "total_meeting_minutes": 160, //总时长
        "rooms" : [
            {
                "host_id" : "ABCDEFGHIJKLMNOPQRSTUVWXYZ", // 公共会议室ID
                "is_extra" : 0,                           // 是否临时添加的会议资源
                "meetings" : 10,                          // 会议总数量
                "participants" : 55,                      // 参会者总数量
                "meeting_minutes" : 10,                   // 会议总时长
                "audio_participants" : 10,                // 音频参会者总数量
                "audio_total_duration" : 120,             // 音频参会者通话总时长，单位分钟
                "total_fee" : 1.2                         // 音频计费总数，单位元
            }
        ]
    }
}
```



