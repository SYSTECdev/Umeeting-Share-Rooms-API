---
description: 删除直播接口，调用该接口后直播后台会把响应的直播删除（不可恢复）
---

# 13、删除直播

## URL <a id="url"></a>

[https://api.systeccloud.com/umeeting/](https://api.systeccloud.com/umeeting/share/schedule)live/{live\_id}/delete

​

## 参数 <a id="&#x53C2;&#x6570;"></a>

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |



## 响应 <a id="&#x54CD;&#x5E94;"></a>

```text
{
    "status": 200,
    "message": "OK",
    "data": null
}
```

