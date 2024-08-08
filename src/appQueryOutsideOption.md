# appQueryOutsideOption
取得查詢欄位"相關單號"的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQueryOutsideOption
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
| request | {'employeeId':'admin','startDate':'20240808', 'endDate':'20240808','vacationType':'1'} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
  "employeeId": "admin",
  "startDate": "20240808",
  "endDate": "20240808",
  "vacationType": "1"
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
| startDate | 20240808 | String | 起始時間 | Y | n/a |
| endDate | 20240808 | String | 結束時間 | Y | n/a |
| vacationType | 1 | String | 請假類別 | Y | n/a |
| employeeId | admin | String | 員工編號 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "outsideIdOption":{
         "name":"相關單號選項",
         "type":"array",
         "value":[
            {
               "name":"相關單號資訊",
               "type":"object",
               "value":{
                  "startDate":{
                     "name":"起始日期",
                     "type":"string",
                     "value":"20240808",
                     "format":"YYYYmmdd",
                     "id":"startDate"
                  },
                  "endDate":{
                     "name":"結束日期",
                     "type":"string",
                     "value":"20240808",
                     "format":"YYYYmmdd",
                     "id":"endDate"
                  },
                  "id":{
                     "name":"相關單號",
                     "type":"string",
                     "value":"GB000202408070001",
                     "format":"n/a",
                     "id":"id"
                  }
               },
               "format":"n/a",
               "id":"outsideId"
            }
         ],
         "format":"n/a",
         "id":"outsideIdOption"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於資料異常，不太可能沒有下拉選項
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
