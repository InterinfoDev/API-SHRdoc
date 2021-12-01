# appAttendDetail
取得某員工可視部門資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appDpetCondition
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
| request | {companyId:97090920 , empid:admin} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "companyId":"97090920",
        "empid":"admin"
    }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | 要求本文 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| empid | admin | String | 員工編號 | Y | n/a |
| companyId | 97090920 | String | 公司別代號 | N | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "id":"depCondition",
         "name":"部門查詢權限",
         "value":[
            {
               "id":"departmentInfo",
               "name":"部門資訊",
               "value":{
                  "companyId":{
                     "id":"companyId",
                     "name":"公司代號",
                     "value":"97090920",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depNumber":{
                     "id":"depNumber",
                     "name":"部門暗碼",
                     "value":1,
                     "type":"integer",
                     "format":"n/a"
                  },
                  "depCode":{
                     "id":"depCode",
                     "name":"部門明碼",
                     "value":"D3200",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depFullName":{
                     "id":"depFullName",
                     "name":"部門全名",
                     "value":"英特內軟體股份有限公司",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depSimpleName":{
                     "id":"depSimpleName",
                     "name":"部門簡稱",
                     "value":"英特內軟體",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depChief":{
                     "id":"depChief",
                     "name":"部門主管",
                     "value":{
                        "empid":{
                           "id":"empid",
                           "name":"員工編號",
                           "value":"L087001",
                           "type":"string",
                           "format":"n/a"
                        },
                        "empName":{
                           "id":"empName",
                           "name":"員工姓名",
                           "value":"李 員",
                           "type":"string",
                           "format":"n/a"
                        }
                     },
                     "type":"object",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
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
