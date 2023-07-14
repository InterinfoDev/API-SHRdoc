# appOvertimeApply
新增實際加班單畫面所需要的資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeApply
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
| request | {startDate:xxx, empid:xxx} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "startDate":"20220413",
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
| startDate | 20220610 | String | 實際加班日期 | N | n/a |
| empid | admin | String | 員工編號 | Y | n/a |

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
            "n/a":""
         }
      },
      "overtime":{
         "name":"當月加班資訊",
         "type":"array",
         "value":[
            {
               "name":"加班總時數",
               "type":"object",
               "value":{
                  "note":{
                     "name":"備註",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"note"
                  },
                  "describe":{
                     "name":"描述標題",
                     "type":"string",
                     "value":"當月已申請加班總時數",
                     "format":"n/a",
                     "id":"describe"
                  },
                  "value":{
                     "name":"總時數",
                     "type":"decimal",
                     "value":0.0,
                     "format":"hour",
                     "id":"value"
                  }
               },
               "format":"n/a",
               "id":"overAmt"
            },
            {
               "name":"加班給薪時數",
               "type":"object",
               "value":{
                  "note":{
                     "name":"備註",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"note"
                  },
                  "describe":{
                     "name":"描述標題",
                     "type":"string",
                     "value":"當月已申請加班給薪時數",
                     "format":"n/a",
                     "id":"describe"
                  },
                  "value":{
                     "name":"給薪時數",
                     "type":"decimal",
                     "value":0.0,
                     "format":"hour",
                     "id":"value"
                  }
               },
               "format":"n/a",
               "id":"overPayHour"
            },
            {
               "name":"加班補休時數",
               "type":"object",
               "value":{
                  "note":{
                     "name":"備註",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"note"
                  },
                  "describe":{
                     "name":"描述標題",
                     "type":"string",
                     "value":"當月已申請加班補休時數",
                     "format":"n/a",
                     "id":"describe"
                  },
                  "value":{
                     "name":"補休時數",
                     "type":"decimal",
                     "value":0.0,
                     "format":"hour",
                     "id":"value"
                  }
               },
               "format":"n/a",
               "id":"overRestHour"
            }
         ],
         "format":"n/a",
         "id":"overtime"
      },
      "note":{
         "name":"備註",
         "type":"object",
         "value":"備註：預定加班單申請完30天內須申請實際加班單，若逾期，則視同放棄。",
         "format":"n/a",
         "id":"note"
      },
      "applyForm":{
         "name":"加班單申請",
         "type":"object",
         "value":{
            "overtimeDate":{
               "name":"實際加班日期",
               "type":"object",
               "value":{
                  "fieldEditable":{
                     "name":"開放編輯",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"fieldEditable"
                  },
                  "fieldValue":{
                     "name":"欄位預設值",
                     "type":"string",
                     "value":"20220610",
                     "format":"YYYYmmdd",
                     "id":"fieldValue"
                  }
               },
               "format":"n/a",
               "id":"overtimeDate"
            },
            "overplanPno":{
               "name":"預定加班單號",
               "type":"object",
               "value":{
                  "option":{
                     "name":"選項",
                     "type":"array",
                     "value":[
                        {   --kevin 新增測試資料
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
                              "value":"補休",
                              "format":"n/a",
                              "id":"optionValue"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"option"
                  },
                  "fieldEditable":{
                      "name":"開放編輯",
                      "type":"boolean",
                      "value":true,
                      "format":"n/a",
                      "id":"fieldEditable"
                   }
               },
               "format":"n/a",
               "id":"overplanPno"
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
