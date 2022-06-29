# appTravelChangeApply
新增出差時程變更申請單畫面所需要的資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelChangeApply
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
| request | Object | 要求本文 |

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
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "day":"天",
            "n/a":""
         }
      },
      "applyForm":{
         "name":"出差變更單申請",
         "type":"object",
         "value":{
            "ApplyTravelChange":{
               "name":"申請出差變更單",
               "type":"object",
               "value":{
                  "option":{
                     "name":"欄位選單項目",
                     "type":"array",
                     "value":[
                        {
                           "optionId":{
                              "name":"選項代號",
                              "type":"string",
                              "value":"K00202206290001-0222(解O庭)-20220629",
                              "format":"n/a",
                              "id":"optionId"
                           },
                           "optionValue":{
                              "name":"選項名稱",
                              "type":"string",
                              "value":"K00202206290001",
                              "format":"n/a",
                              "id":"optionValue"
                           }
                        },
                        {
                           "optionId":{
                              "name":"選項代號",
                              "type":"string",
                              "value":"K00202206070002-0442(詹O郁)-20220609",
                              "format":"n/a",
                              "id":"optionId"
                           },
                           "optionValue":{
                              "name":"選項名稱",
                              "type":"string",
                              "value":"K00202206070002",
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
               "id":"applyTravelChange"
            }
         },
         "format":"n/a",
         "id":"applyForm"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，不會有查無資料情況
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
