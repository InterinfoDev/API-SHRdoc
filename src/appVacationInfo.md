# appVacationInfo
取得所選假別使用情況

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationInfo
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
| request | {empid:9306020,vacationCode:39,specialDate: } | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326", 
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"9306020",
        "vacationCode":"39",
        "specialDate":""
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
| empid | 9306020 | string | 員工編號 | Y | n/a |
| hcode | 39 | string | 假別代碼 | N | n/a |
| specialDate |  | string | 特殊日期 | N | YYMMDD |

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
      "vacationDetail":{
         "name":"假別資訊",
         "type":"array",
         "value":[
            {
               "name":"當年度疫苗接種假資訊",
               "type":"array",
               "value":[
                  {
                     "name":"當年度疫苗接種假",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"當年度疫苗接種假",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"32.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"total"
                  },
                  {
                     "name":"已休(含在途)",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"已休(含在途)",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"0.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"applied"
                  },
                  {
                     "name":"未休",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"未休",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"32.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"applied"
                  }
               ],
               "format":"n/a",
               "id":"vacationInfo"
            },
            {
               "name":"颱風假資訊",
               "type":"array",
               "value":[
                  {
                     "name":"當年度疫苗接種假",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"當年度颱風假",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"無上限",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"total"
                  },
                  {
                     "name":"已休(含在途)",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"已休(含在途)",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"0.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"applied"
                  },
                  {
                     "name":"未休",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"未休",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"無上限",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"applied"
                  }
               ],
               "format":"n/a",
               "id":"vacationInfo"
            },
            {
               "name":"選舉/罷免假資訊",
               "type":"array",
               "value":[
                  {
                     "name":"當年度疫苗接種假",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"當次選舉/罷免假",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"0.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"total"
                  },
                  {
                     "name":"已休(含在途)",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"已休(含在途)",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"0.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"applied"
                  },
                  {
                     "name":"未休",
                     "type":"object",
                     "value":{
                        "describe":{
                           "name":"描述標題",
                           "type":"string",
                           "value":"未休",
                           "format":"n/a",
                           "id":"describe"
                        },
                        "noteOfVaction":{
                           "name":"備註",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"noteOfVaction"
                        },
                        "valueOfVaction":{
                           "name":"假期數量",
                           "type":"string",
                           "value":"0.00",
                           "format":"hour",
                           "id":"valueOfVaction"
                        }
                     },
                     "format":"n/a",
                     "id":"applied"
                  }
               ],
               "format":"n/a",
               "id":"vacationInfo"
            }
         ],
         "format":"n/a",
         "id":"vacationDetail"
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
