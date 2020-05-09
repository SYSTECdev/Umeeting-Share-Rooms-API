# 预约会议接口

---

### URL

[https://api.systeccloud.com/umeeting/share/schedule](https://api.systeccloud.com/umeeting/share/schedule)

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| topic | 是 | String | 会议主题 |
| meeting\_capacity | 是 | Integer | 会议方数 |
| start\_time | 是 | String | 开始时间，格式如：2017-08-19 00:00:00 |
| duration | 是 | Integer | 会议持续时间，以分钟为单位，必须大于30 |
| password | 否 | String | 会议密码 |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |
| mute\_upon\_entry | 否 | String | true:入会时静音，false:入会时不静音 |
| use\_pmi | 否 | String | true/false使用个人会议号预约（特殊条件，需要有特定的账号） |
| option\_host\_video | 否 | String | true/false |
| option\_participants\_video | 否 | String | true/false |
| recording | 否 | String | "cloud"-表示云端录制，“none"-表示不录制，默认不录制 |
| host\_name | 否 | String | 主持人名称 |
| allow\_live\_streaming | 否 | String | "true"-开启直播推流，“false"-不开启直播推流 （默认”false" |
| waiting\_room | 否 | String | "true"-与会者入会时需要主持人允许后才能入会，“false"-与会者入会时不需要主持人的允许便可加入会议 |

### 响应

```js
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
       "watch_url": "https://wx.vzan.com/live/tvchat-1590377657?ver=637223897808876626"     // 观看地址

    }
}
```



