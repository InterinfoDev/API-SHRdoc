# appTravelChangeList
查詢單一員工該年月區間的出差變更資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelList
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
| request | {travelYM:202203, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的員工及畫面上的年月取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "travelChangeYM":"202201", 
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
| travelYM | 202201 | String | 查詢年月 | Y | AC(YYYYmm) |
| empid | admin | String | 員工編號 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"出差變更資訊",
         "type":"object",
         "value":{
            "travelChangeYM":{
               "name":"出差年月",
               "type":"string",
               "value":"202203",
               "format":"YYYYmm",
               "id":"travelChangeYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "employee":{
         "name":"員工基本資料",
         "type":"object",
         "value":{
            "position":{
               "name":"職稱",
               "type":"string",
               "value":"系統管理員",
               "format":"n/a",
               "id":"position"
            },
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系統管理員",
               "format":"n/a",
               "id":"empFullName"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "depFullName":{
               "name":"部門名稱",
               "type":"string",
               "value":"英特內股份有限公司",
               "format":"n/a",
               "id":"depFullName"
            },
            "empFullEname":{
               "name":"員工英文姓名",
               "type":"string",
               "value":"Administrator",
               "format":"n/a",
               "id":"empFullEname"
            }
         },
         "format":"n/a",
         "id":"employee"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "travelChangeList":{
         "name":"員工出差變更列表",
         "type":"array",
         "value":[
            {
               "name":"員工出差變更資訊",
               "type":"object",
               "value":{
                  "startTime":{
                     "name":"出差起始時間",
                     "type":"string",
                     "value":"0800",
                     "format":"HHmm",
                     "id":"startTime"
                  },
                  "startDate":{
                     "name":"出差起日",
                     "type":"string",
                     "value":"20220304",
                     "format":"YYYYmmdd",
                     "id":"startDate"
                  },
                  "travelPlace":{
                     "name":"出差地點名稱",
                     "type":"string",
                     "value":"新竹",
                     "format":"n/a",
                     "id":"travelPlace"
                  },
                  "pno":{
                     "name":"變更單號",
                     "type":"string",
                     "value":"K00202203040001",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "version":{
                     "name":"變更版次",
                     "type":"string",
                     "value":"1.2",
                     "format":"n/a",
                     "id":"version"
                  },
                  "applyDate":{
                     "name":"申請日期",
                     "type":"string",
                     "value":"20220307",
                     "format":"YYYYmmdd",
                     "id":"applyDate"
                  },
                  "oldPno":{
                     "name":"出差單號",
                     "type":"string",
                     "value":"K00202203040001",
                     "format":"n/a",
                     "id":"oldPno"
                  },
                  "endDate":{
                     "name":"出差迄日",
                     "type":"string",
                     "value":"20220307",
                     "format":"YYYYmmdd",
                     "id":"endDate"
                  },
                  "endTime":{
                     "name":"出差結束時間",
                     "type":"string",
                     "value":"1700",
                     "format":"HHmm",
                     "id":"endTime"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approved"
                  },
                  {
                     "amt":{
                        "name":"總計",
                        "type":"string",
                        "value":"8.00",
                        "format":"hour",
                        "id":"amt"
                      }
                  }
               },
               "format":"n/a",
               "id":"travel"
            },
         ],
         "format":"n/a",
         "id":"travelChangeList"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
