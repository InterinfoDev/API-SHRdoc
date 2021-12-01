# appSalaryRecent
取得某員工最近一次薪資發放資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSalaryRecent
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
| request | {empid:admin} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin"
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
| empid | admin | String | 員工編號 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salaryRecent":{
         "id":"salaryRecentInfo",
         "name":"最近一次薪資發放資訊",
         "value":{
            "ym":{
               "id":"ym",
               "name":"薪資年月",
               "value":"202109",
               "type":"string",
               "format":"YYYYmm"
            },
            "count":{
               "id":"count",
               "name":"計薪次數",
               "value":"1",
               "type":"integer",
               "format":"count"
            },
            "indate":{
               "id":"indate",
               "name":"入帳日期",
               "value":"20211105",
               "type":"string",
               "format":"YYYYmmdd"
            }
         },
         "type":"object",
         "format":"n/a"
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
