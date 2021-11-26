# appEmployeeCondition

取得可視範圍員工資料

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appEmployeeCondition
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
| **uid**   | String | 加密後帳號 |
| **right** | String | 加密後系統相關資料 |
| **request** | 要求本文 |

### request Properties

| Key | Value | Type | Description
|:----------|:-------------|:-----|:------------|


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "id":"employeeCondition",
         "name":"人員查詢權限",
         "value":[
            {
               "id":"employeeInfo",
               "name":"員工資訊",
               "value":{
                  "empName":{
                     "id":"empName",
                     "name":"員工中文姓名",
                     "value":"林奇杰",
                     "type":"string",
                     "format":"n/a"
                  },
                  "empEname":{
                     "id":"empEname",
                     "name":"員工英文姓名",
                     "value":"Lucas",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depNumber":{
                     "id":"deoCode",
                     "name":"部門暗碼",
                     "value":2,
                     "type":"integer",
                     "format":"n/a"
                  },
                  "depCode":{
                     "id":"deoCode",
                     "name":"部門代號",
                     "value":"D2000",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depName":{
                     "id":"depName",
                     "name":"部門名稱",
                     "value":"CTO",
                     "type":"string",
                     "format":"n/a"
                  },
                  "empid":{
                     "id":"empid",
                     "name":"員工編號",
                     "value":"L100387",
                     "type":"string",
                     "format":"n/a"
                  },
                  "position":{
                     "id":"position",
                     "name":"職稱",
                     "value":"CTO",
                     "type":"string",
                     "format":"n/a"
                  },
                  "photo":{
                     "id":"photo",
                     "name":"員工照片",
                     "value":"base64url",
                     "type":"string",
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
    "code": 406,
    "message": [
        "系統錯誤"
    ],
    "data": {}
}
```
