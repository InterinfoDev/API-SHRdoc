# appAllDepartment
取得目前有在使用的全部部門

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAllDepartment
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
| request | {companyId:97090920} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "companyId":"97090920"
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
| companyId | 97090920 | String | 公司別代號 | N | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "allDepartment":{
         "id":"allDepartment",
         "name":"全部部門",
         "value":[
            {
               "id":"department",
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
                        "empFullName":{
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
