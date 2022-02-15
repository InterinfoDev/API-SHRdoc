# appFlowTodoList
取得使用者待簽核單據

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowTodoList
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
      "HRFlowTodoList":{
         "id":"HRFlowTodoList",
         "name":"待簽核單據",
         "value":[
            {
               "id":"CA3",
               "name":"CA3.個人資料維護覆核",
               "type":"object",
               "value":[
                  {
                     "flowCount":{
                        "id":"flowCount",
                        "name":"節點數量",
                        "value":1,
                        "type":"integer",
                        "format":"count"
                     },
                     "flowState":{
                        "id":"flowState",
                        "name":"節點名稱",
                        "value":"申請人",
                        "type":"string",
                        "format":"n/a"
                     }
                  }
               ],
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "count":"次數",
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
