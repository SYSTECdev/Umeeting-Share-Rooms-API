# 绑定个人账号

---

### URL

[https://api.systeccloud.com/umeeting/user/](https://api.systeccloud.com/umeeting/share/schedule)delete

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| email | 是 | String | 账号邮箱 |

### 响应

```js
{
    "status" : 200,                   // 状态码，200为成功，其他值为失败
    "message" : "OK",                 // 本次请求结果信息，如果为错误时，即为详细的错误信息 
     "data": {
        "host_key": "367260",         //主持人key
        "meeting_capacity": "25",     //会议方数
        "id": "2-Vhs-ODRstEXupxQ",    //hostId
        "email": "share3@systec.com.cn", //邮箱
        "token": "2xFiocLpU177HG8MDgxzk4MwAMM0NCQXVvaVlTM3M9" //开会token
    }  
}
```



