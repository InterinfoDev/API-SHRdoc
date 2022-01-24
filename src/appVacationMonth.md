# appVacationMonth
查詢員工請假資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationMonth
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| request | {depNumber:[5], vacationYM:202108, empid:[admin], companyId:TW, hcode:15} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "vacationYM":"202108", 
        "companyId":"TW",
        "hcode":"15",
        "depNumber":[5], 
        "empid":["admin"]
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
| vacationYM | 202108 | String | 查詢年月 | Y | AC(YYYYmm) |
| companyId | TW | String | 公司代號 | N | n/a |
| hcode | 15 | String | 假別代碼 | N | n/a |
| depNumber | [5] | Array(Integer) | 部門代號 | N | n/a |
| empid | [admin] | Array(String) | 員工編號 | N | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"請假年月資訊",
         "type":"object",
         "value":{
            "vacationYM":{
               "name":"請假年月",
               "type":"string",
               "value":"202201",
               "format":"YYYYmm",
               "id":"vacationYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "vacationList":{
         "name":"員工請假列表",
         "type":"array",
         "value":[
            {
               "name":"員工請假資訊",
               "type":"object",
               "value":{
                  "photo":{
                     "name":"員工相片",
                     "type":"string",
                     "value":"",
                     "format":"base64",
                     "id":"photo"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "vacationYM":{
                     "name":"請假年月",
                     "type":"string",
                     "value":"202201",
                     "format":"YYYYmm",
                     "id":"vacationYM"
                  },
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"position"
                  },
                  "unapproved":{
                     "name":"簽核中",
                     "type":"integer",
                     "value":2,
                     "format":"count",
                     "id":"unapproved"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系O管",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"L1線A班",
                     "format":"n/a",
                     "id":"depFullName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"admin000",
                     "format":"n/a",
                     "id":"empFullEname"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"integer",
                     "value":0,
                     "format":"count",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"vacationInfo"
            }
         ],
         "format":"n/a",
         "id":"vacationList"
      },
      "properties":{
         "format":{
            "base64":"Base64編碼格式",
            "count":"數量",
            "n/a":"",
            "YYYYmm":"西元年月"
         }
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
    "status": "success",
    "message": [
        "查無資料"
    ],
    "data": {
        "main": {
            "name": "請假年月資訊",
            "type": "object",
            "value": {
                "vacationYM": {
                    "name": "請假年月",
                    "type": "string",
                    "value": "202201",
                    "format": "YYYYmm",
                    "id": "vacationYM"
                }
            },
            "format": "n/a",
            "id": "main"
        },
        "vacationList": {
            "name": "員工請假列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "vacationList"
        },
        "properties": {
            "format": {
                "base64": "Base64編碼格式",
                "count": "數量",
                "n/a": "",
                "YYYYmm": "西元年月"
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
