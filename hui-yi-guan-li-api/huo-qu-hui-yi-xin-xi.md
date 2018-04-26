# 获取会议信息接口

---

### URL

[https://api.systeccloud.com/umeeting/share/get](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_id | 是 | String | 会议号 |

### 响应

```js
{
    "status" : 200,  // 状态码，200为成功，其他值为失败
    "message" : "OK" // 本次请求结果信息，如果为错误时，即为详细的错误信息
     "data": {
        "duration": "50",                   //会议时长
        "start_time": "2018-04-26 15:00:00",//开始时间
        "del_flag": "0",                    //删除标志 0 正常 1 已删除            
        "password": "",                     //会议密码
        "topic": "王者荣耀世界大战",          //会议主题
        "user_Key": null,                   //用户身份key 
        "meeting_capacity": "25",           //会议方数 
        "id": "1574054185",                 //会议号
        "status": "0"                       //会议状态 0 已预约 1 会议进行中 2 已取消 3 已结束 
    }
}
```



