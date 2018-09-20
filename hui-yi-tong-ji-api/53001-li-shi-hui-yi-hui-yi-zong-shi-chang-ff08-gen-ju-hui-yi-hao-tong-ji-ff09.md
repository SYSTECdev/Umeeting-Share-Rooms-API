# 历史会议会议总时长（根据会议号统计）

---

### URL

[https://api.systeccloud.com/umeeting/share/meetingTime](https://api.systeccloud.com/umeeting/share/meetingTime)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 是 | String | 标准格式时间 "2018-01-01" |
| to | 是 | String | 标准格式时间 “2018-01-01” |

### 响应

```js
    "status": 200,
    "message": "OK",
    "data": [
        {
            "id": "1376669196",                    //会议号
            "time": 9                              //分钟
        },
        {
            "id": "1396312207",
            "time": 2
        },
        {
            "id": "1397639071",
            "time": 4
        },
        {
            "id": "1355911723",
            "time": 3
        },
        {
            "id": "1584985950",
            "time": 7
        }
    }
```



