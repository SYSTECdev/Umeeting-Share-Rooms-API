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

## 响应

```javascript
{
    "status": 200,                                 // 状态码，200为成功，其他值为失败
    "message": "OK",                               // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "host_key": "765418",                      //主持人密钥
        "join_url": "https://**/j/1591620888",     //入会链接
        "meeting_id": "1591620888",                // 会议号
        "start_time": "",                          // 开始时间
        "host_id": "mueyYP0sQp-",                  //主持人hostId
        "token": "9AYkPEIrxUzZmU2ZWIQXVvaVlTM3M9"，  //开会token
        "start_url": "https://u.systeccloud.com/s/1890181373?zak=eyJ6bV9za20iOiJ6bV9vMm0iLCJh
           bGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiJjbGllbnQiLCJ1aWQiOiJMLXpMcXFxd1FfaWVtVUlqZ
           TE3UDBRIiwiaXNzIjoid2ViIiwic3R5IjoxMDAsIndjZCI6InN5IiwiY2x0IjowLCJzdGsiOiJuaWtkOG53STN
           0TkRlZ2ZRU3FWeHhiMGhwX2swVFJkUmpfUk00YUlhbmtjLkJnVTRUMGxOUm1ReVZtRjZjRXRsUWpOUmIyU
           TJibkZyVEdFeGJHOUZTMnR4VVc1QmFFNWlhREZ2VFd0cFZFaGFhRWRwUzFneFdWcEJQVDFBTVdZMU1UUmxOem
           xpTmpjNVpXVmpPV00yWmpBek9XTTNOR0U1WlRKbU4yRTNPVEZsWldRNU1ESXhPRE5oTmpZMVlUSmlPR1UyTURW
           ak5qZzRNRE5tTndBTU0wTkNRWFZ2YVZsVE0zTTlBQUp6ZVEiLCJleHAiOjE1ODUxMzIzNzcsImlhdCI6MTU4NTE
           yNTE3NywiYWlkIjoiUkZVaVFOVUtRVG0tbXFfcHNCeFludyIsImNpZCI6IiJ9.-qzrBzHf66b06ruZpt4
           gK2bzh6kZUXcEhmuvUOsofJs",                 // start_url，慎用
       "play_addr": "http://p2.weizan.cn/79555295/132312377802785197/live.m3u8",             // 视频地址
       "watch_url": "https://wx.vzan.com/live/tvchat-1590377657?ver=637223897808876626"      // 观看地址

    }
}
```

