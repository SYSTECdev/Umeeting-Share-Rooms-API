# 查询指定SA网络会议许可

---

### URL

[https://api.systeccloud.com/umeeting/](https://api.systeccloud.com/umeeting/share/schedule)licensing

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |

### 响应

```js
{
    "status": 200,
    "message": "OK",
    "data": {
        "payType": "1", // 1.表示方数计费，2.并发参会者计费方式 3 使用时长计费 
        "expire_date": null,
        "capacity": {
            "100": 3,
            "200": 1,
            "25": 5,
            "300": 0,
            "500": 0,
            "50": 55,
            "10": 11
        }
    }
}
```



