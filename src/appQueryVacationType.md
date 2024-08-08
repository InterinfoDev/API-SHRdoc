# appQueryVacationType
取得請假請假類別的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQueryVacationType
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

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "vacationTypeOption":{
         "name":"請假類別選項",
         "type":"array",
         "value":[
            {
               "name":"請假類別資訊",
               "type":"object",
               "value":{
                  "typeName":{
                     "name":"請假類別名稱",
                     "type":"string",
                     "value":"其他",
                     "format":"n/a",
                     "id":"typeName"
                  },
                  "typeCode":{
                     "name":"請假類別代碼",
                     "type":"string",
                     "value":"3",
                     "format":"n/a",
                     "id":"typeCode"
                  }
               },
               "format":"n/a",
               "id":"vacationType"
            },
            {
               "name":"請假類別資訊",
               "type":"object",
               "value":{
                  "typeName":{
                     "name":"請假類別名稱",
                     "type":"string",
                     "value":"大陸（不含港澳）",
                     "format":"n/a",
                     "id":"typeName"
                  },
                  "typeCode":{
                     "name":"請假類別代碼",
                     "type":"string",
                     "value":"1",
                     "format":"n/a",
                     "id":"typeCode"
                  }
               },
               "format":"n/a",
               "id":"vacationType"
            },
            {
               "name":"請假類別資訊",
               "type":"object",
               "value":{
                  "typeName":{
                     "name":"請假類別名稱",
                     "type":"string",
                     "value":"其他國家（含港澳）",
                     "format":"n/a",
                     "id":"typeName"
                  },
                  "typeCode":{
                     "name":"請假類別代碼",
                     "type":"string",
                     "value":"2",
                     "format":"n/a",
                     "id":"typeCode"
                  }
               },
               "format":"n/a",
               "id":"vacationType"
            }
         ],
         "format":"n/a",
         "id":"vacationTypeOption"
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
