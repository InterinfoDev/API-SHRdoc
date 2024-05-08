# appIrregularOvertimeViewType
取得查詢條件顯示種類的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimeViewType
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
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "viewType":{
         "name":"顯示種類",
         "type":"object",
         "value":{
            "option":{
               "name":"選項",
               "type":"array",
               "value":[
                  {
                     "optionId":{
                        "name":"選項代號",
                        "type":"string",
                        "value":"A",
                        "format":"n/a",
                        "id":"optionId"
                     },
                     "optionValue":{
                        "name":"選項名稱",
                        "type":"string",
                        "value":"顯示所有異常",
                        "format":"n/a",
                        "id":"optionValue"
                     }
                  },
                  {
                     "optionId":{
                        "name":"選項代號",
                        "type":"string",
                        "value":"B",
                        "format":"n/a",
                        "id":"optionId"
                     },
                     "optionValue":{
                        "name":"選項名稱",
                        "type":"string",
                        "value":"顯示每一天的紀錄",
                        "format":"n/a",
                        "id":"optionValue"
                     }
                  }
               ],
               "format":"n/a",
               "id":"option"
            }
         },
         "format":"n/a",
         "id":"viewType"
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
