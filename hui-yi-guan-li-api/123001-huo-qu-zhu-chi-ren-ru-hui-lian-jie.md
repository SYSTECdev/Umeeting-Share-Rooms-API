# 12、获取主持人入会连接

（只有在会议到了提前入会时间才会返回该连接）

## URL <a id="url"></a>

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)getStartUrl

## 参数 <a id="&#x53C2;&#x6570;"></a>

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| id | 是 | String | 会议号 |

## 响应 <a id="&#x54CD;&#x5E94;"></a>

```text
{
    "status" : 200,  // 状态码，200为成功，其他值为失败
    "message" : "OK" // 本次请求结果信息，如果为错误时，即为详细的错误信息
    "data": {
        "start_url": "https://demosso.systeccloud.com/s/15455452?zak=eyJ6bV9V9vMm0iLCJhbGci....."  // 开始会议连接
    } 
}
```

