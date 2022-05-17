# appQueryReason
取得補卡原因的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQueryReason
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
Here is a JSON representation of request.
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
      "reasonOption":{
         "name":"補卡原因選項",
         "type":"array",
         "value":[
            {
               "name":"補卡原因資訊",
               "type":"object",
               "value":{
                  "reasonName":{
                     "name":"補卡原因內容",
                     "type":"string",
                     "value":"忘刷卡",
                     "format":"n/a",
                     "id":"reasonName"
                  },
                  "reasonCode":{
                     "name":"補卡原因代碼",
                     "type":"string",
                     "value":"001",
                     "format":"n/a",
                     "id":"reasonCode"
                  }
               },
               "format":"n/a",
               "id":"reason"
            },
            {
               "name":"補卡原因資訊",
               "type":"object",
               "value":{
                  "reasonName":{
                     "name":"補卡原因內容",
                     "type":"string",
                     "value":"忘記帶卡",
                     "format":"n/a",
                     "id":"reasonName"
                  },
                  "reasonCode":{
                     "name":"補卡原因代碼",
                     "type":"string",
                     "value":"002",
                     "format":"n/a",
                     "id":"reasonCode"
                  }
               },
               "format":"n/a",
               "id":"reason"
            }
         ],
         "format":"n/a",
         "id":"reasonOption"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於資料異常，不太可能沒有下拉選項
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
