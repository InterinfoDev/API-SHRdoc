# appQueryAgentFunction
取得代理簽核的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQueryAgentFunction
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
    "right":"51341911904173543336756162544864820",
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
      "functionOption":{
         "name":"代理功能選項",
         "type":"array",
         "value":[
            {
               "name":"代理功能資訊",
               "type":"object",
               "value":{
                  "functionName":{
                     "name":"代理功能內容",
                     "type":"string",
                     "value":"C.126.個人工作目標修改簽核",
                     "format":"n/a",
                     "id":"functionName"
                  },
                  "functionCode":{
                     "name":"代理功能代碼",
                     "type":"string",
                     "value":"590535521097405056829363076749951101069612102461523530525384772277901512134546",
                     "format":"n/a",
                     "id":"functionCode"
                  }
               },
               "format":"n/a",
               "id":"function"
            },
            {
               "name":"代理功能資訊",
               "type":"object",
               "value":{
                  "functionName":{
                     "name":"代理功能內容",
                     "type":"string",
                     "value":"C.221.績效考核表簽核",
                     "format":"n/a",
                     "id":"functionName"
                  },
                  "functionCode":{
                     "name":"代理功能代碼",
                     "type":"string",
                     "value":"32819584023378686730886652136667731359480025202980105526370",
                     "format":"n/a",
                     "id":"functionCode"
                  }
               },
               "format":"n/a",
               "id":"function"
            }
         ],
         "format":"n/a",
         "id":"functionOption"
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
