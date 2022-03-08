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
      "HRFlowTodoList":{
         "name":"待簽核單據",
         "type":"array",
         "value":[
            {
               "name":"CA3.個人資料維護覆核",
               "type":"array",
               "value":[
                  {
                     "name":"節點資訊",
                     "type":"object",
                     "value":{
                        "flowCount":{
                           "name":"節點數量",
                           "type":"integer",
                           "value":1,
                           "format":"count",
                           "id":"flowCount"
                        },
                        "flowState":{
                           "name":"節點名稱",
                           "type":"string",
                           "value":"申請人",
                           "format":"n/a",
                           "id":"flowState"
                        },
                        "flowKey":{
                           "name":"節點鍵值",
                           "type":"string",
                           "value":"640130555211610131235169414143042796600194383642310910304424435998404931445693",
                           "format":"n/a",
                           "id":"flowKey"
                        }
                     },
                     "format":"n/a",
                     "id":"flow"
                  }
               ],
               "format":"n/a",
               "id":"CA3.個人資料維護覆核"
            }
         ],
         "format":"n/a",
         "id":"HRFlowTodoList"
      }
   }
}
```

### HTTP Response when No Data 
```json
{
    "status": "success",
    "message": [
        "查無資料"
    ],
    "data": {
        "HRFlowTodoList": {
            "name": "待簽核單據",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "HRFlowTodoList"
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
