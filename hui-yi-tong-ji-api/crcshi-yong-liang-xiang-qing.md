# CRC使用量详情

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)crcUsage

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 是 | String | yyyy-MM-dd |
| to | 是 | String | yyyy-MM-dd \(to要大于from；如果要查询12-01，那么from就是12-01to就要为12-02） |

### 响应

```
{
```

```js
    "status": 200,
    "message": "OK",
    "data": [
        {
            "date_time": "2019-12-01",
            "crc_ports_hour_usage": [
                {
                    "hour": "00",
                    "max_usage": 0,
                    "total_usage": 0
                },
                {
                    "hour": "01",
                    "max_usage": 1,
                    "total_usage": 1
                },
                {
                    "hour": "02",
                    "max_usage": 1,
                    "total_usage": 4
                },
                ...
                ...
                ...
                ...
        },
        {
            "date_time": "2019-12-02",
            "crc_ports_hour_usage": [
                {
                    "hour": "00",
                    "max_usage": 1,
                    "total_usage": 1
                },
                {
                    "hour": "01",
                    "max_usage": 11,
                    "total_usage": 13
                },
                ...
                ...
                ...
        }
    ]
}
```



