# 3、空闲会议室查询接口

## URL

[https://api.systeccloud.com/umeeting/share/freeRooms](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_capacity | 是 | Integer | 会议方数 |
| start\_time | 是 | String | 开始时间，格式如：2017-08-19 00:00:00 |
| duration | 是 | Integer | 会议持续时间，以分钟为单位，必须大于30 |

## 响应

```javascript
{
    "status": 200,                                 //状态码，200为成功，其他值为失败
    "message": "OK",                               // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "total": 8,                                //该方数的会议室总数
        "free": 8                                  //空闲会议室数
    }
}
```

