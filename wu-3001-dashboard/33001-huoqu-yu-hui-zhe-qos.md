# 3、获取与会者qos

## URL

[https://api.systeccloud.com/umeeting](https://api.systeccloud.com/umeeting/share/schedule)/metrics/participants/qos

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| uuid | 是 | String | 会议uuid（可以会议详情列表接口里获取） |
| type | 否 | String | live—在线（默认），past—结束 |
| user\_id | 是 | String | 该参数是Dashboard中获取与会者接口中返回的user\_id |

## 响应

```javascript
{
    "status": 200,
    "message": "OK",
    "data": [
        {
            "date_time": "2020-01-10T07:56:00Z",                                       （注意这里是UTC格式）
            "audio_input": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": ""
            },
            "audio_output": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": ""
            },
            "video_input": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": "",
                "resolution": "",
                "frame_rate": ""
            },
            "video_output": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": "",
                "resolution": "",
                "frame_rate": ""
            },
            "as_input": {
                "bitrate": "138 kbps",
                "latency": "10 ms",
                "jitter": "615 ms",
                "avg_loss": "0.0%",
                "max_loss": "0.0%",
                "resolution": "",
                "frame_rate": ""
            },
            "as_output": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": "",
                "resolution": "",
                "frame_rate": ""
            },
            "cpu_usage": {
                "zoom_min_cpu_usage": "3%",
                "zoom_avg_cpu_usage": "3%",
                "zoom_max_cpu_usage": "6%",
                "system_max_cpu_usage": "72%"
            }
        },
        .....
        .....
        .....
        {
            "date_time": "2020-01-10T07:57:00Z",
            "audio_input": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": ""
            },
            "audio_output": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": ""
            },
            "video_input": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": "",
                "resolution": "",
                "frame_rate": ""
            },
            "video_output": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": "",
                "resolution": "",
                "frame_rate": ""
            },
            "as_input": {
                "bitrate": "72 kbps",
                "latency": "11 ms",
                "jitter": "391 ms",
                "avg_loss": "0.0%",
                "max_loss": "0.0%",
                "resolution": "",
                "frame_rate": ""
            },
            "as_output": {
                "bitrate": "",
                "latency": "",
                "jitter": "",
                "avg_loss": "",
                "max_loss": "",
                "resolution": "",
                "frame_rate": ""
            },
            "cpu_usage": {
                "zoom_min_cpu_usage": "3%",
                "zoom_avg_cpu_usage": "4%",
                "zoom_max_cpu_usage": "6%",
                "system_max_cpu_usage": "51%"
            }
        }

    ]
}
```

