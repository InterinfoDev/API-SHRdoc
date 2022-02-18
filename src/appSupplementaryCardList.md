# appSupplementaryCardList
查詢單一員工該年月區間的補卡資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardList
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
| request | {cardYM:202111, empid:admin} | Object | 查詢條件

### JSON representation
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cardYM":"2021906"
        "empid":"admin",
    }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### Request Properties
 Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| empid | admin | String | 員工編號 | Y | n/a | 查詢員工編號 |
| cardYM | 202106 | String | 查詢年月 | Y | AC(YYYYmm) |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"補卡資訊",
         "type":"object",
         "value":{
            "cardYM":{
               "name":"補卡年月",
               "type":"string",
               "value":"202106",
               "format":"YYYYmm",
               "id":"cardYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "user":{
         "name":"員工基本資料",
         "type":"object",
         "value":{
            "position":{
               "name":"職稱",
               "type":"string",
               "value":"短期契約",
               "format":"n/a",
               "id":"position"
            },
            "photo":{
               "name":"員工相片",
               "type":"string",
               "value":"",
               "format":"base64",
               "id":"photo"
            },
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系O管",
               "format":"n/a",
               "id":"empFullName"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "depFullName":{
               "name":"部門名稱",
               "type":"string",
               "value":"L1線A班",
               "format":"n/a",
               "id":"depFullName"
            },
            "empFullEname":{
               "name":"員工英文姓名",
               "type":"string",
               "value":"test_Ename",
               "format":"n/a",
               "id":"empFullEname"
            }
         },
         "format":"n/a",
         "id":"user"
      },
      "cardList":{
         "name":"員工補卡列表",
         "type":"array",
         "value":[
            {
               "name":"員工補卡資訊",
               "type":"object",
               "value":{
                  "addDate":{
                     "name":"申請日期",
                     "type":"string",
                     "value":"20210629",
                     "format":"YYYYmmdd",
                     "id":"addDate"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "supplementaryCardKey":{
                     "name":"單據編號",
                     "type":"string",
                     "value":"20210600000000000002",
                     "format":"n/a",
                     "id":"supplementaryCardKey"
                  },
                  "reason":{
                     "name":"補登原因",
                     "type":"string",
                     "value":"忘刷卡",
                     "format":"n/a",
                     "id":"reason"
                  },
                  "cardDate":{
                     "name":"補卡日期",
                     "type":"string",
                     "value":"20210601",
                     "format":"YYYYmmdd",
                     "id":"cardDate"
                  },
                  "cardTime":{
                     "name":"補卡時間",
                     "type":"string",
                     "value":"0600",
                     "format":"HHmm",
                     "id":"cardTime"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系O管",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "depCode":{
                     "name":"部門明碼",
                     "type":"string",
                     "value":"14121",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"card"
            },
            {
               "name":"員工補卡資訊",
               "type":"object",
               "value":{
                  "addDate":{
                     "name":"申請日期",
                     "type":"string",
                     "value":"20210610",
                     "format":"YYYYmmdd",
                     "id":"addDate"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "pno":{
                     "name":"單據編號",
                     "type":"string",
                     "value":"20210600000000000001",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "reason":{
                     "name":"補登原因",
                     "type":"string",
                     "value":"忘刷卡",
                     "format":"n/a",
                     "id":"reason"
                  },
                  "cardDate":{
                     "name":"補卡日期",
                     "type":"string",
                     "value":"20210610",
                     "format":"YYYYmmdd",
                     "id":"cardDate"
                  },
                  "cardTime":{
                     "name":"補卡時間",
                     "type":"string",
                     "value":"0830",
                     "format":"HHmm",
                     "id":"cardTime"
                  },
                  "cardType": {
                    "name": "進出別",
                    "type": "string",
                    "value": "進卡",
                    "format": "n/a",
                    "id": "cardType"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系O管",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "depCode":{
                     "name":"部門明碼",
                     "type":"string",
                     "value":"14121",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"card"
            }
         ],
         "format":"n/a",
         "id":"cardList"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "base64":"Base64編碼格式",
            "YYYYmmdd":"西元年月日",
            "n/a":""
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
