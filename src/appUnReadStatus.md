# appUnReadStatus
查詢各通知類別未讀取資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appUnReadStatus
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
| request | {} | Object | 查詢條件

### JSON representation
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
    }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "readNotification":{
         "name":"推播資訊",
         "type":"object",
         "value":{
            "sysUnRead":{
               "name":"系統通知是否有未讀資訊",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"sysUnRead"
            },
            "hrUnRead":{
               "name":"訊息通知是否有未讀資訊",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"hrUnRead"
            },
            "flowUnRead":{
               "name":"系統簽核通知是否有未讀資訊",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"flowUnRead"
            }
         },
         "format":"n/a",
         "id":"readNotification"
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
