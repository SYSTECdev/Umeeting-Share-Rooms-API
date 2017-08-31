# 公共会议室明细统计接口

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)daily/detail

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 否 | String | 统计起始时间，默认为当天 |
| to | 否 | String | 统计结束时间，默认为当天 |
| host\_id | 否 | String | 公共会议室ID，如果没有指定，则查询所有公共会议室的明细信息 |
| page\_size | 否 | Integer | 分页显示，每页大小，不指定时为30 |
| page\_number | 否 | Integer | 分页显示，第几页，不指定时为1 |

### 响应

```js
{
    "status" : 200,                  // 状态码，200为成功，其他值为失败
    "message" : "OK",                // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "from" : "2017-8-31", 
        "to" : "2017-09-01", 
        "total_record" : 1, 
        "total_page" : 1, 
        "page_number" : 1, 
        "page_size" : 30, 
        "has_previous_page" : false,
        "has_next_page" : false,
        "meetings" : [
            {
                "host_id" : "ABCDEFGHIJKLMNOPQRSTUVWXYZ", 
                "meeting_id" : "1790001234", 
                "topic" : "Hello world!", 
                "start_time" : "2017-08-31 00:00:00", 
                "duration" : 120, 
                "end_time" : "2017-08-31 01:00:00", 
                "is_extra" : 0, 
                "participants" : [
                ], 
                "telep" : [{

                    }, 
                    {
                }]
            }
        ]
    }
}
```



