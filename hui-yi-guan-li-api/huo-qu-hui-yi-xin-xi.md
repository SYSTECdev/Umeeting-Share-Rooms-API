# 3、获取会议信息接口

## URL

[https://api.systeccloud.com/umeeting/share/get](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| meeting\_id | 是 | String | 会议号 |

## 响应

```javascript
{
    "status" : 200,  // 状态码，200为成功，其他值为失败
    "message" : "OK" // 本次请求结果信息，如果为错误时，即为详细的错误信息
     "data": {
        "occurrences": [                      // 周期性会议
            {
                "start_time": "2020-05-18 15:00:00",
                "uuid": "3mv9ja4i3xm1duop495mzy=="
            },
            {
                "start_time": "2020-05-19 15:00:00",
                "uuid": "y5arrbltdrhr9b5xwlbbo3=="
            },
            {
                "start_time": "2020-05-20 15:00:00",
                "uuid": "3m7z72lklzg7bz25tudbki=="
            },
            {
                "start_time": "2020-05-21 15:00:00",
                "uuid": "mhxbomci9xtphsjndir5j6=="
            },
            {
                "start_time": "2020-05-22 15:00:00",
                "uuid": "pqv62tr7x9qoheu3jg3w7e=="
            }
        ],
        "duration": "50",                   //会议时长
        "start_time": "2018-04-26 15:00:00",//开始时间
        "del_flag": "0",                    //删除标志 0 正常 1 已删除            
        "password": "",                     //会议密码
        "join_url":""                       //入会链接
        "topic": "王者荣耀世界大战",          //会议主题
        "user_Key": null,                   //用户身份key 
        "meeting_capacity": "25",           //会议方数 
        "id": "1574054185",                 //会议号
        "status": "0",                      //会议状态 0 已预约 1 会议进行中 2 已取消 3 已结束 
        "allow_live_streaming": "true",
        "play_addr": "http://p2.weizan.cn/79555295/132312361257166751/live.m3u8"",        //视频地址
        "watch_url": "https://wx.vzan.com/live/tvchat-315528467?ver=637223881258260609"   //观看地址
    }
}
```

