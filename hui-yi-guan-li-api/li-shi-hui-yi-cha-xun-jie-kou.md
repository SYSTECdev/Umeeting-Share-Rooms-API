# 8、历史会议查询接口 \(废弃）

## URL

[https://api.systeccloud.com/umeeting/share/history](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| user\_key | 否 | String | 指定该参数时，获取与该参数相关联的在线会议信息，否则获取所有在线会议信息 |
| page\_size | 否 | Integer | 分页显示，每页大小，不指定时默认为30 |
| page\_number | 否 | Integer | 分页显示，第几页，不指定时默认为1 |

## 响应

```javascript
{
    "status" : 200,                               // 状态码，200为成功，其他值为失败
    "message" : "OK",                             // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "page_num" : 1,                           // 分页显示的页码
        "page_size" : 30,                         // 分页显示的每页显示记录数
        "total_record" : 1,                       // 记录总数
        "total_page" : 1,                         // 共计多少页
        "has_previous_page" : false,              // 是否有前一页
        "has_next_page" : false                   // 是否有后一页
        "meetings": [{
            "duration" : 20,                      // 会议持续时间
            "start_time" : "2017-08-15 00:00:00", // 会议开始时间
            "topic" : "HelloWorld!",              // 会议主题
            "id" : "1360671085",                  // 会议号
            "status": 1                           // 会议状态，2-已取消，3-已结束
            "host_key": "030488", //主持人密钥
            "type": "2" //会议类型 1 即时会议 2 预约的会议
        }]
    }
}
```

