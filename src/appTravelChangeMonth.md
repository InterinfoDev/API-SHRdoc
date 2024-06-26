# appTravelChangeMonth
查詢員工出差變更資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravellChangeMonth
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
| request | {depNumber:[], travelYM:202203, empid:[admin], companyId:TW} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "travelChangeYM":"202203", 
        "companyId":"TW",
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
| travelYM | 202203 | String | 查詢年月 | Y | AC(YYYYmm) |
| companyId | TW | String | 公司代號 | N | n/a |
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
         "name":"出差變更資訊",
         "type":"object",
         "value":{
            "travelChangeYM":{
               "name":"出差年月",
               "type":"string",
               "value":"202203",
               "format":"YYYYmm",
               "id":"travelChangeYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "properties":{
         "format":{
            "count":"數量",
            "n/a":"",
            "YYYYmm":"西元年月",
            "hyperlink":"超連結"
         }
      },
      "travelList":{
         "name":"員工出差變更列表",
         "type":"array",
         "value":[
            {
               "name":"員工出差變更資訊",
               "type":"object",
               "value":{
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"position"
                  },
                   "photo": {
                     "name": "員工照片",
                     "type": "string",
                     "value": "http://59.124.100.151:8090/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f1a574d52104f57504b50100e0909070f0b0b0607070b0b07600e0b0f070f060e0e0d114f5158",
                     "format": "hyperlink",
                     "id": "photo"
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
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"integer",
                     "value":0,
                     "format":"count",
                     "id":"approved"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"英特內股份有限公司",
                     "format":"n/a",
                     "id":"depFullName"
                  }
               },
               "format":"n/a",
               "id":"travel"
            },
            {
               "name":"員工出差變更資訊",
               "type":"object",
               "value":{
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"position"
                  },
                  "photo": {
                     "name": "員工照片",
                     "type": "string",
                     "value": "http://59.124.100.151:8090/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f1a574d52104f57504b50100e0909070f0b0b0607070b0b07600e0b0f070f060e0e0d114f5158",
                     "format": "hyperlink",
                     "id": "photo"
                  },
                  "unapproved":{
                     "name":"簽核中",
                     "type":"integer",
                     "value":0, 
                     "format":"count",
                     "id":"unapproved"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"二號同仁",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"RT002",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"integer",
                     "value":1,
                     "format":"count",
                     "id":"approved"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"SKT-0329",
                     "format":"n/a",
                     "id":"depFullName"
                  }
               },
               "format":"n/a",
               "id":"travel"
            }
         ],
         "format":"count",
         "id":"travelList"
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
