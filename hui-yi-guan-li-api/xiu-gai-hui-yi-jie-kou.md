---
description: >-
  （如果修改周期会议，仅支持修改整个系列会议，不支持修改周期会议里面的单个会议；同时修改会议可以将普通会议修改为周期会议，只需要传相应的周期属性，如果需要将周期会议修改为普通会议，传参示例：
  ”recurrence_type": ""    即可)
---

# 4、修改会议接口

## URL

[https://api.systeccloud.com/umeeting/share/update](https://api.systeccloud.com/umeeting/share/schedule)

## 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| id | 是 | String | 会议号 |
| topic | 否 | String | 会议主题 |
| start\_time | 是 | String | 会议开始时间，yyyy-MM-dd  HH:mm:ss |
| duration | 是 | Integer | 会议持续时间（分钟） |
| password | 否 | String | 会议密码 |
| user\_key | 否 | String | 用户身份自定义信息，用于标识预约会议用户身份，不能超过200字节 |
| mute\_upon\_entry | 否 | String | true: 入会时静音，false: 入会时不静音 |
| recording | 否 | String | "cloud"-云端录制，”none"-不录制，默认不录制 |
| allow\_live\_streaming | 否 | String | "true"-开启直播推流，”false"-关闭直播推流（默认"false"） |
| host\_name | 否 | String | 主持人名称 |
| waiting\_room | 否 | String | "true"-与会者入会时需要主持人允许后才能入会，“false"-与会者入会时不需要主持人的允许便可加入会议 |
| recurrence\_type | 否 | Integer | 周期会议类型 1-按天，2-按周，3-按月 （非周期会议不传或者传""（空）\) |
| daily\_type | 否 | Integer | （周期会议按天属性）1-每天，2-工作日 |
| weekly\_days | 否 | String | \(周期会议按周属性）示例：“1，3”，表示每周1，3重复 |
| monthly\_week | 否 | integer | \(周期会议按月属性）每个月的第几个星期（取值范围1-5），配合monthly\_week\_day使用，表示每个月的第几个星期的星期几 |
| monthly\_week\_day | 否 | Integer | \(周期会议按月属性）每个月的某个星期的星期几（取值范围1-7），配合monthly\_week使用，表示每个月的第几个星期的星期几 |
| monthly\_day | 否 | Integer | \(周期会议按月属性）每个月的几号重复（取值范围1-31），这个的优先值大于monthly\_week的设置，如果monthly\_week，monthly\_day同时存在，则以monthly\_day为主 |

## 响应

```javascript
{
    "status" : 200,  // 状态码，200为成功，其他值为失败
    "message" : "OK" // 本次请求结果信息，如果为错误时，即为详细的错误信息
}
```

