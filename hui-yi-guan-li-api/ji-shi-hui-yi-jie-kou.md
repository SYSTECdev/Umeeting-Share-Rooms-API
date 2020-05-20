# 2、即时会议接口

[https://api.systeccloud.com/umeeting/share/instant](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| topic | 是 | String | 会议主题 |
| option\_jbh | 否 | String | 允许主持人入会前加入会议，true/false，true为允许，false为不允许 |
| meeting\_capacity | 是 | Integer | 会议方数 |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |
| duration | 否 | Integer | 会议持续时间，以分钟为单位，必须大于30 |
| mute\_upon\_entry | 否 | String | true: 入会时静音，false：入会时不静音 |
| use\_pmi | 否 | String | true/false ,使用个人会议号（特定条件） |
| option\_host\_video | 否 | String | true/false |
| option\_participants\_video | 否 | String | true/false |
| recording | 否 | String | "cloud"-云端录制，“none"-不录制，默认不录制 |
| allow\_live\_streaming | 否 | String | "true"-开启直播推流，“false"-关闭直播推流（ |
| host\_name | 否 | String | 主持人名称 |
| waiting\_room | 否 | String | "true"-与会者入会时需要主持人允许后才能入会，“false"-与会者入会时不需要主持人的允许便可加入会议 |
| recurrence\_type | 否 | Integer | 周期会议类型 1-按天，2-按周，3-按月 （非周期会议不传或者传""（空）\) |
| daily\_type | 否 | Integer | （周期会议按天属性）1-每天，2-工作日 |
| weekly\_days | 否 | String | \(周期会议按周属性）示例：“1，3”，表示每周1，3重复 |
| monthly\_week | 否 | integer | \(周期会议按月属性）每个月的第几个星期（取值范围1-5），配合monthly\_week\_day使用，表示每个月的第几个星期的星期几 |
| monthly\_week\_day | 否 | Integer | \(周期会议按月属性）每个月的某个星期的星期几（取值范围1-7），配合monthly\_week使用，表示每个月的第几个星期的星期几 |
| monthly\_day | 否 | Integer | \(周期会议按月属性）每个月的几号重复（取值范围1-31），这个的优先值大于monthly\_week的设置，如果monthly\_week，monthly\_day同时存在，则以monthly\_day为主 |
|  |  |  |  |

## 响应

```javascript
{
    "status": 200,                                  //状态码，200为成功，其他值为失败
    "message": "OK",                                // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "host_key": "030488",                       //主持人密钥
        "join_url": "https://**/j/1770498237",      //入会链接
        "meeting_id": "1770498237",                 //会议号  
        "start_time": "7",                          //会议开始时间   
        "host_id": "8Eki6-0R7eVsdg-mH4y7A",         //主持人hostId
        "token": "fTlrrST1Ve8iLAMM0NCQXVvaVlTM3M9", //开始会议token
        "mute_upon_entry": "true",
        "ready_time": 15,                            //提前入会时间
        "start_url": "https://u.systeccloud.com/s/1890181373?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJh
           bGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1aWQiOiJMLXpMcXFxd1FfaWVtVUlqZ
           TE3UDBRIiwiaXNzIjoid2ViIiwic3R5IjoxMDAsIndjZCI6InN5IiwiY2x0IjowLCJzdGsiOiJuaWtkOG53STN
           0TkRlZ2ZRU3FWeHhiMGhwX2swVFJkUmpfUk00YUlhbmtjLkJnVTRUMGxOUm1ReVZtRjZjRXRsUWpOUmIyU
           TJibkZyVEdFeGJHOUZTMnR4VVc1QmFFNWlhREZ2VFd0cFZFaGFhRWRwUzFneFdWcEJQVDFBTVdZMU1UUmxOem
           xpTmpjNVpXVmpPV00yWmpBek9XTTNOR0U1WlRKbU4yRTNPVEZsWldRNU1ESXhPRE5oTmpZMVlUSmlPR1UyTURW
           ak5qZzRNRE5tTndBTU0wTkNRWFZ2YVZsVE0zTTlBQUp6ZVEiLCJleHAiOjE1ODUxMzIzNzcsImlhdCI6MTU4NTE
           yNTE3NywiYWlkIjoiUkZVaVFOVUtRVG0tbXFfcHNCeFludyIsImNpZCI6IiJ9.-qzrBzHf66b06ruZpt4
           gK2bzh6kZUXcEhmuvUOsofJs",                 // start_url，慎用
       "play_addr": "http://p2.weizan.cn/79555295/132312377802785197/live.m3u8",            // 视频地址
       "watch_url": "https://wx.vzan.com/live/tvchat-1590377657?ver=637223897808876626",     // 观看地址
       "live_id": "12345663",    //直播号
       "occurrences": [                                 // 周期会议列表
            {
                "start_time": "2020-05-18 10:00:00",     // 会议开始时间
                "uuid": "2d3l1sotx4rky8vcipkrku=="       // 每个会议的uuid（唯一）
            },
            {
                "start_time": "2020-05-19 10:00:00",
                "uuid": "9fqqv0gx57zgj83wy2pzra=="
            },
            {
                "start_time": "2020-05-20 10:00:00",
                "uuid": "1cyrs8qs2bxtq9gp115e6x=="
            }
        ]

    }
}
```

