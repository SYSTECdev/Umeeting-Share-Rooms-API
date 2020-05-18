# 7、获取会议云端录制信息

## URL

[https://api.systeccloud.com/](https://api.systeccloud.com/umeeting/share/meetingTime)umeeting/cloud/recording

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| start\_time | 是 | String | 标准格式时间 如“2020-02-02 14:25:12” |
| meeting\_id | 是 | String | 这里可以是会议号，也可以是会议记录的uuid（一场会议里面可能有多条会议记录，每天会议记录都会有唯一的uuid），会议记录需要同步历史会议记录 |

## 响应

```javascript
    {
    "status": 200,
    "message": "OK",
    "data": [
        {
            "id": "cc8bc310-4bcb-42d3-bf35-2f2ef01f9be4",
            "meeting_id": "Jn5K/PTATp+WjU071OuceA==",                        // 会议uuid
            "recording_start": "2020-02-13T09:28:41Z",
            "recording_end": "2020-02-13T09:30:34Z",
            "file_type": "MP4",
            "file_size": 2748588,
            "play_url": "https://umeetingdev.systeccloud.com/recording/play/5MoKVVAxj3yen1wP8kh3YSxt4BJBSDrr29jrovwDamAL-yBcqI2YTbNvLK8h6exW",            // 播放地址
            "download_url": "https://umeetingdev.systeccloud.com/recording/download/5MoKVVAxj3yen1wP8kh3YSxt4BJBSDrr29jrovwDamAL-yBcqI2YTbNvLK8h6exW",    // 下载地址
            "status": "completed"
        },
        {
            "id": "1e30b902-2dc6-4deb-9f98-9bec13342764",
            "meeting_id": "zPGZC+dXTeqHsT61Y/wqrg==",
            "recording_start": "2020-02-13T10:19:50Z",
            "recording_end": "2020-02-13T10:20:57Z",
            "file_type": "MP4",
            "file_size": 174511,
            "play_url": "https://umeetingdev.systeccloud.com/recording/play/Ogc6sUt__IpDozayoUOo5EAG4aVeCQqSqjOM5kjVF9OsvwyMK2eYMxyyeZZkU0bZ",
            "download_url": "https://umeetingdev.systeccloud.com/recording/download/Ogc6sUt__IpDozayoUOo5EAG4aVeCQqSqjOM5kjVF9OsvwyMK2eYMxyyeZZkU0bZ",
            "status": "completed"
        }
    ]
}
```

