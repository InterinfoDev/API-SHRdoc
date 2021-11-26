# appSalaryCountQuery

取得公司薪資發放次數資訊

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appSalaryCountQuery
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
| **uid**   | String | 加密後帳號 |
| **right** | String | 加密後系統相關資料 |
| **request** | 要求本文 |

### request Properties

| Key | Value | Type | Description
|:----------|:-------------|:-----|:------------|
| empid | admin| String | 員工編號 |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salaryCountInfo":{
         "id":"salaryCountInfo",
         "name":"查詢薪資發放次數資訊",
         "value":[
            {
               "id":"salaryCoun",
               "name":"發放次數",
               "value":1,
               "type":"integer",
               "format":"times"
            },
            {
               "id":"salaryCoun",
               "name":"發放次數",
               "value":2,
               "type":"integer",
               "format":"times"
            },
            {
               "id":"salaryCoun",
               "name":"發放次數",
               "value":3,
               "type":"integer",
               "format":"times"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":"",
            "times":"次數"
         }
      }
   }
}
```

### HTTP Response when Failed
```json
{
    "status": "fail",
    "code": 406,
    "message": [
        "系統錯誤"
    ],
    "data": {}
}
```
