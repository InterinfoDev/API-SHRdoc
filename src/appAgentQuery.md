# appAgentQuery
取得代理人清單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAgentQuery
```

### HTTP Request Method
```
POST
```

### Request body
| Property | Type | Description |
|:---------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {employeeId:admin} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "employeeId":"admin"
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
| employeeId | admin | String | 被代理人 | N | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "agentList":{
         "name":"人員查詢權限",
         "type":"array",
         "value":[
            {
               "name":"員工資訊",
               "type":"object",
               "value":{
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"班長(一)",
                     "format":"n/a",
                     "id":"position"
                  },
                  "depCode":{
                     "name":"部門代號",
                     "type":"string",
                     "value":"15700",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "photo":{
                     "name":"員工照片",
                     "type":"string",
                     "value":"",
                     "format":"base64",
                     "id":"photo"
                  },
                  "depNumber":{
                     "name":"部門暗碼",
                     "type":"integer",
                     "value":31,
                     "format":"n/a",
                     "id":"depNumber"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"弓O倫",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"0006",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "depName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"行銷部",
                     "format":"n/a",
                     "id":"depName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"NEW0006",
                     "format":"n/a",
                     "id":"empFullEname"
                  }
               },
               "format":"n/a",
               "id":"employee"
            },
            {
               "name":"員工資訊",
               "type":"object",
               "value":{
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"position"
                  },
                  "depCode":{
                     "name":"部門代號",
                     "type":"string",
                     "value":"16112",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "photo":{
                     "name":"員工照片",
                     "type":"string",
                     "value":"",
                     "format":"base64",
                     "id":"photo"
                  },
                  "depNumber":{
                     "name":"部門暗碼",
                     "type":"integer",
                     "value":42,
                     "format":"n/a",
                     "id":"depNumber"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"何O以",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"0018",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "depName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"L1b班",
                     "format":"n/a",
                     "id":"depName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"何宣以",
                     "format":"n/a",
                     "id":"empFullEname"
                  }
               },
               "format":"n/a",
               "id":"employee"
            }
         ],
         "format":"n/a",
         "id":"agentList"
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
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
