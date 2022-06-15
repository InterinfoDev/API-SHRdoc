# appOvertimeMonth
查詢員工實際加班資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeMonth
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
| request | {depNumber:[5], overtimeYM:202201, empid:[admin], companyId':TW} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "overplanYM":"202104", 
        "companyId":"TW",
        "depNumber":[89], 
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
| overplanYM | 202108 | String | 查詢年月 | Y | AC(YYYYmm) |
| companyId | TW | String | 公司代號 | N | n/a |
| depNumber | [89] | Array(Integer) | 部門代號 | N | n/a |
| empid | [admin] | Array(String) | 員工編號 | N | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "overtimeList":{
         "name":"員工實際加班列表",
         "type":"array",
         "value":[
            {
               "name":"員工實際加班資訊",
               "type":"object",
               "value":{
                  "position":{
                     "name":"職稱",
                     "type":"string",
                     "value":"行政",
                     "format":"n/a",
                     "id":"position"
                  },
                  "overtimeYM":{
                     "name":"實際加班年月",
                     "type":"string",
                     "value":"202209",
                     "format":"YYYYmm",
                     "id":"overtimeYM"
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
                     "value":"一號同仁",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"RT001",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"integer",
                     "value":2,
                     "format":"count",
                     "id":"approved"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"奇亞零三二九部門",
                     "format":"n/a",
                     "id":"depFullName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"empFullEname"
                  }
               },
               "format":"n/a",
               "id":"overtime"
            }
         ],
         "format":"n/a",
         "id":"overtimeList"
      },
      "properties":{
         "format":{
            "count":"數量",
            "n/a":"",
            "YYYYmm":"西元年月"
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
