# appFlowNotify
取得簽核單據數量

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowNotify
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
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "count":"數量",
            "n/a":""
         }
      },
      "flowNotify":{
         "name":"待簽核單據",
         "type":"object",
         "value":{
            "notifyConut":{
               "name":"待簽核單據",
               "type":"integer",
               "value":"81",
               "format":"count",
               "id":"notifyConut"
            }
         },
         "format":"n/a",
         "id":"flowNotify"
      }
   }
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
