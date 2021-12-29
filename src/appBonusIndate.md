# appBonusIndate 
取得員工指定年月獎金入帳日期資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBonusIndate
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {} | Object | 查詢條件 |


### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ "salbondYM":"202111"
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
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| salbondYM | 202111 | String | 獎金年月 | Y | AC(YYYYmm) |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "bonusIndate":{
         "name":"獎金入帳日期資訊",
         "type":"array",
         "value":[
            {
               "name":"入帳日期",
               "type":"string",
               "value":"20131001",
               "format":"YYYYmmdd",
               "id":"indate"
            }
         ],
         "format":"n/a",
         "id":"bonusIndate"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，所以回傳空陣列
```json
{
   "status":"success",
   "message":[
      "查無資料"
   ],
   "data":{
      "bonusIndate":{
         "name":"獎金入帳日期資訊",
         "type":"array",
         "value":[],
         "format":"n/a",
         "id":"bonusIndate"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "n/a":""
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
