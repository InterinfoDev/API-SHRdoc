# appSupplementaryCardMonth
取得員工補卡資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardMonth
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
| request | {cardYM:202111, empid:admin , depNumber:[], state:false} | Object | 查詢條件

### JSON representation
Case 1 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cardStartDate":"20210603",
        "cardEndDate":"20220302",
        "empid":"",
        "depNumber":[]
    }
}
```
Case 2 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cardYM":"2021906"
        "empid":"",
        "depNumber":[]
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
| Case No | Key | Value | Type | Description | Required | Format |
|:----------|:----------|:-------------|:-----|:------------|:------------|:------------|
|   | empid | admin | String | 員工編號 | N | n/a | 查詢員工編號 |
|   | depNumber | [5] | Array(Integer) | 部門代號 | N | n/a |
|   | state | false | boolean | 是否生效 | N | 已生效:true、未生效:false、全部:不放此欄位|
|   | cardYM | 202106 | String | 查詢年月 | Y | AC(YYYYmm) |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"請假資訊",
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
      "cardList":{
         "name":"員工補卡列表",
         "type":"array",
         "value":[
            {
               "name":"員工補卡資訊",
               "type":"object",
               "value":{
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"短期契約",
                     "format":"n/a",
                     "id":"position"
                  },
                  "unapproved":{
                     "name":"簽核中",
                     "type":"integer",
                     "value":2,
                     "format":"count",
                     "id":"unapproved"
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
                  "approved":{
                     "name":"已生效",
                     "type":"integer",
                     "value":0,
                     "format":"count",
                     "id":"approved"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"L1線A班",
                     "format":"n/a",
                     "id":"depFullName"
                  }
               },
               "format":"n/a",
               "id":"card"
            }
         ],
         "format":"count",
         "id":"cardList"
      },
      "properties":{
         "format":{
            "count":"數量",
            "n/a":"",
            "YYYYmm":"西元年月"
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "supplementaryCard": {
            "name": "補卡資訊",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "supplementaryCard"
        },
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        }
    }
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
