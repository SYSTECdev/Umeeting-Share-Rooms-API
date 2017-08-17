# 在线会议查询接口（Coming soon）

---

### URL

[https://api.systeccloud.com/umeeting/share/list](https://api.systeccloud.com/umeeting/share/schedule)

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
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data" : {
        "meeting_id" : "15464648254", // 会议号
        "host_id" : "",               // 主持人账号ID，由SDK调用
        "token" : ""                  // 主持人账号Token，有SDK调用
    }
}
```



