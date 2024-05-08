# appExpireFlowAgent
刪除簽核代理人資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appExpireFlowAgent
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {'flowAgentKey':XXXXXXXXX} | Object | 異動條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "flowAgentKey":"XXXXXXXXX"
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| flowAgentKey | true | boolean | 單據編號 | true | n/a |  |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "flowAgent":{
         "name":"刪除簽核代理人",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"異動成功",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
            }
         },
         "format":"n/a",
         "id":"flowAgent"
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
