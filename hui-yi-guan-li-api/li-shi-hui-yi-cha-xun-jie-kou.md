# 历史会议查询接口（Coming soon）

---

### URL

[https://api.systeccloud.com/umeeting/share/his](https://api.systeccloud.com/umeeting/share/schedule)tory

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secure | 是 | String | API secure |
| user\_key | 否 | String | 指定该参数时，获取与该参数相关联的在线会议信息，否则获取所有在线会议信息 |
| page\_size | 否 | Integer | 分页显示，每页大小，不指定时默认为30 |
| page\_number | 否 | Integer | 分页显示，第几页，不指定时默认为1 |

### 响应

```js
{
    "status" : 200,                               // 状态码，200为成功，其他值为失败
    "message" : "OK",                             // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "total" : 1,                              // 记录总数
        "meetings" : [{
            "id" : "15464648254",                 // 会议号
            "topic" : "",                         // 会议主题
            "status" : 2,                         // 会议状态，2-已取消，3-已结束
            "start_time" : "2017-08-17 00:00:00", // 开始时间
            "end_time" : "2017-08-17 00:15:31"    // 结束时间，会议未开始被取消，结束时间为空
        }]
    }
}
```



