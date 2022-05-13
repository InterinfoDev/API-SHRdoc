# appFlowAgentList
查詢簽核代理人資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowAgentList
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820"
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|



### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "flowAgentList": {
            "name": "簽核代理人列表",
            "type": "array",
            "value": [
                {
                    "name": "簽核代理人資訊",
                    "type": "object",
                    "value": {
                        "function": {
                            "name": "代理功能",
                            "type": "string",
                            "value": "C.126.個人工作目標修改簽核",
                            "format": "n/a",
                            "id": "function"
                        },
                        "endTime": {
                            "name": "代理結束時間",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "endTime"
                        },
                        "key": {
                            "name": "資料索引值",
                            "type": "string",
                            "value": "12487659774168172618768299574942949518028740856953495932069812901468259930334017116152477345615391",
                            "format": "n/a",
                            "id": "key"
                        },
                        "agent": {
                            "name": "代理人",
                            "type": "string",
                            "value": "1355",
                            "format": "n/a",
                            "id": "agent"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "鞏O倫",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "0091",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "starTime": {
                            "name": "代理起始時間",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "starTime"
                        },
                        "agentName": {
                            "name": "簽核代理人姓名",
                            "type": "string",
                            "value": "廣O佑廣O佑廣O佑廣O佑",
                            "format": "n/a",
                            "id": "agentName"
                        }
                    },
                    "format": "n/a",
                    "id": "flowAgent"
                },
                {
                    "name": "簽核代理人資訊",
                    "type": "object",
                    "value": {
                        "function": {
                            "name": "代理功能",
                            "type": "string",
                            "value": "C.221.績效考核表簽核",
                            "format": "n/a",
                            "id": "function"
                        },
                        "endTime": {
                            "name": "代理結束時間",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "endTime"
                        },
                        "key": {
                            "name": "資料索引值",
                            "type": "string",
                            "value": "676957392820648821866873594550406547788033845224824634457511768246772113272956",
                            "format": "n/a",
                            "id": "key"
                        },
                        "agent": {
                            "name": "代理人",
                            "type": "string",
                            "value": "1355",
                            "format": "n/a",
                            "id": "agent"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "鞏O倫",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "0091",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "starTime": {
                            "name": "代理起始時間",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "starTime"
                        },
                        "agentName": {
                            "name": "簽核代理人姓名",
                            "type": "string",
                            "value": "廣O佑廣O佑廣O佑廣O佑",
                            "format": "n/a",
                            "id": "agentName"
                        }
                    },
                    "format": "n/a",
                    "id": "flowAgent"
                },
                {
                    "name": "簽核代理人資訊",
                    "type": "object",
                    "value": {
                        "function": {
                            "name": "代理功能",
                            "type": "string",
                            "value": "CB2.1.請假單簽核",
                            "format": "n/a",
                            "id": "function"
                        },
                        "endTime": {
                            "name": "代理結束時間",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "endTime"
                        },
                        "key": {
                            "name": "資料索引值",
                            "type": "string",
                            "value": "676957392820648821864061521739683258360670551866432903124883108368712720808379",
                            "format": "n/a",
                            "id": "key"
                        },
                        "agent": {
                            "name": "代理人",
                            "type": "string",
                            "value": "1355",
                            "format": "n/a",
                            "id": "agent"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "鞏O倫",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "0091",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "starTime": {
                            "name": "代理起始時間",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "starTime"
                        },
                        "agentName": {
                            "name": "簽核代理人姓名",
                            "type": "string",
                            "value": "廣O佑廣O佑廣O佑廣O佑",
                            "format": "n/a",
                            "id": "agentName"
                        }
                    },
                    "format": "n/a",
                    "id": "flowAgent"
                },
                {
                    "name": "簽核代理人資訊",
                    "type": "object",
                    "value": {
                        "function": {
                            "name": "代理功能",
                            "type": "string",
                            "value": "CB2.1.請假單簽核",
                            "format": "n/a",
                            "id": "function"
                        },
                        "endTime": {
                            "name": "代理結束時間",
                            "type": "string",
                            "value": "2021/11/15 17:00",
                            "format": "n/a",
                            "id": "endTime"
                        },
                        "key": {
                            "name": "資料索引值",
                            "type": "string",
                            "value": "71498905997051669694753916033137341108492672005024160321966725331425988946949725447985873788481599525941015944043333500432156022369644099311372573508609826",
                            "format": "n/a",
                            "id": "key"
                        },
                        "agent": {
                            "name": "代理人",
                            "type": "string",
                            "value": "10600009",
                            "format": "n/a",
                            "id": "agent"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "仇O淇",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "0179",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "starTime": {
                            "name": "代理起始時間",
                            "type": "string",
                            "value": "2021/11/15 08:00",
                            "format": "n/a",
                            "id": "starTime"
                        },
                        "agentName": {
                            "name": "簽核代理人姓名",
                            "type": "string",
                            "value": "tOs",
                            "format": "n/a",
                            "id": "agentName"
                        }
                    },
                    "format": "n/a",
                    "id": "flowAgent"
                },
                {
                    "name": "簽核代理人資訊",
                    "type": "object",
                    "value": {
                        "function": {
                            "name": "代理功能",
                            "type": "string",
                            "value": "CB3.1.預定加班單簽核",
                            "format": "n/a",
                            "id": "function"
                        },
                        "endTime": {
                            "name": "代理結束時間",
                            "type": "string",
                            "value": "2021/11/15 17:00",
                            "format": "n/a",
                            "id": "endTime"
                        },
                        "key": {
                            "name": "資料索引值",
                            "type": "string",
                            "value": "1318922020477829207708895623245226786531961598600155888092460583400417610830859686463248350654580523202444694870817122770689412621515639398604557069248679713693666346271799572",
                            "format": "n/a",
                            "id": "key"
                        },
                        "agent": {
                            "name": "代理人",
                            "type": "string",
                            "value": "10600009",
                            "format": "n/a",
                            "id": "agent"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "仇O淇",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "0179",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "starTime": {
                            "name": "代理起始時間",
                            "type": "string",
                            "value": "2021/11/15 08:00",
                            "format": "n/a",
                            "id": "starTime"
                        },
                        "agentName": {
                            "name": "簽核代理人姓名",
                            "type": "string",
                            "value": "tOs",
                            "format": "n/a",
                            "id": "agentName"
                        }
                    },
                    "format": "n/a",
                    "id": "flowAgent"
                },
                {
                    "name": "簽核代理人資訊",
                    "type": "object",
                    "value": {
                        "function": {
                            "name": "代理功能",
                            "type": "string",
                            "value": "C7.補刷卡簽核",
                            "format": "n/a",
                            "id": "function"
                        },
                        "endTime": {
                            "name": "代理結束時間",
                            "type": "string",
                            "value": "2021/08/16 09:00",
                            "format": "n/a",
                            "id": "endTime"
                        },
                        "key": {
                            "name": "資料索引值",
                            "type": "string",
                            "value": "1294143037927171846250089652033520070204300974014762329594157127711705907151744731551158571970519968584468106957973952459179741229495042765223515949543391484075044390781699291",
                            "format": "n/a",
                            "id": "key"
                        },
                        "agent": {
                            "name": "代理人",
                            "type": "string",
                            "value": "10600009",
                            "format": "n/a",
                            "id": "agent"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "單O申",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "applytest001",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "starTime": {
                            "name": "代理起始時間",
                            "type": "string",
                            "value": "2021/08/16 08:00",
                            "format": "n/a",
                            "id": "starTime"
                        },
                        "agentName": {
                            "name": "簽核代理人姓名",
                            "type": "string",
                            "value": "tOs",
                            "format": "n/a",
                            "id": "agentName"
                        }
                    },
                    "format": "n/a",
                    "id": "flowAgent"
                }
            ],
            "format": "n/a",
            "id": "flowAgentList"
        },
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "hour": "小時",
                "YYYYmmdd": "西元年月日",
                "day": "天",
                "n/a": ""
            }
        }
    }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "查無資料"
    ],
    "data": {}
}
```

### HTTP Response when Failed
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "XXX"
    ],
    "data": {}
}
```

### HTTP Response when Exception
```json
{
    "status": "fail",
    "code": 406,
    "message": [
        "XXX"
    ],
    "data": {}
}
```
