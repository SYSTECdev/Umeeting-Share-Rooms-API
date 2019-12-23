# CRC使用量详情

---

### URL

[https://api.systeccloud.com/umeeting/share/](https://api.systeccloud.com/umeeting/share/schedule)crcUsage

### 参数

| 参数名称 | 是否必须 | 参数类型 | 描述 |
| :--- | :--- | :--- | :--- |
| api\_key | 是 | String | API key |
| api\_secret | 是 | String | API secret |
| from | 是 | String | yyyy-MM-dd |
| to | 是 | String | yyyy-MM-dd \(to要大于from；如果要查询12-01，那么from就是12-01to就要为12-02） |

### 响应

{

	"status": 200,

	"message": "OK",

	"data": \[{

		"date\_time": "2019-12-01",

		"crc\_ports\_hour\_usage": \[{

				"hour": "00",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "01",

				"max\_usage": 1,

				"total\_usage": 1

			},

			{

				"hour": "02",

				"max\_usage": 1,

				"total\_usage": 4

			},

			{

				"hour": "03",

				"max\_usage": 1,

				"total\_usage": 1

			},

			{

				"hour": "04",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "05",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "06",

				"max\_usage": 1,

				"total\_usage": 1

			},

			{

				"hour": "07",

				"max\_usage": 1,

				"total\_usage": 1

			},

			{

				"hour": "08",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "09",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "10",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "11",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "12",

				"max\_usage": 1,

				"total\_usage": 2

			},

			{

				"hour": "13",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "14",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "15",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "16",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "17",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "18",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "19",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "20",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "21",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "22",

				"max\_usage": 0,

				"total\_usage": 0

			},

			{

				"hour": "23",

				"max\_usage": 1,

				"total\_usage": 1

			}

		\]

	}\]

}





