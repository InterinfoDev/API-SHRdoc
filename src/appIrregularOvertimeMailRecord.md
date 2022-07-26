# appIrregularOvertimeMailRecord
取得加班異常信件通知紀錄

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimeMailRecord
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
| request | {irregularYM:202207, empid:admin} | Object | 查詢條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "irregularYM":"202104",     -- richard 修改request key值 irregularYM
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
| irregularYM | 202104 | String | 查詢年月 | Y | AC(YYYYmm) |  
| empid | admin | String | 員工編號 | N | n/a |

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
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "dayofweek":"星期"
         }
      },
      "sendMailList":{
         "name":"信件通知列表",
         "type":"array",
         "value":[
            {
               "name":"員工加班異常資訊",
               "type":"object",
               "value":{
                  "source":{
                     "name":"來源",
                     "type":"string",
                     "value":"報表",
                     "format":"n/a",
                     "id":"source"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "sendChief":{
                     "name":"寄發員工主管",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"sendChief"
                  },
                  "sendDate":{
                     "name":"寄發日期",
                     "type":"boolean",
                     "value":"20220708",
                     "format":"YYYYmmdd",
                     "id":"sendDate"
                  },
                  "empFullName":{
                     "name":"員工姓名",
                     "type":"string",
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "sendTime":{
                     "name":"寄發時間",
                     "type":"string",
                     "value":"0922",
                     "format":"HHmm",
                     "id":"sendTime"
                  },
                  "errorDate":{
                     "name":"異常日期",
                     "type":"string",
                     "value":"20220701",
                     "format":"YYYYmmdd",
                     "id":"errorDate"
                  },
                  "sendPersonnel":{
                     "name":"寄發員工本人",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"sendPersonnel"
                  },
                  "result":{
                     "name":"寄發結果",
                     "type":"string",
                     "value":"成功",
                     "format":"n/a",
                     "id":"result"
                  }
               },
               "format":"n/a",
               "id":"sendMailList"
            },
            {
               "name":"員工加班異常資訊",
               "type":"object",
               "value":{
                  "source":{
                     "name":"來源",
                     "type":"string",
                     "value":"報表",
                     "format":"n/a",
                     "id":"source"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "sendChief":{
                     "name":"寄發員工主管",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"sendChief"
                  },
                  "sendDate":{
                     "name":"寄發日期",
                     "type":"string",
                     "value":"20220708",
                     "format":"YYYYmmdd",
                     "id":"sendDate"
                  },
                  "empFullName":{
                     "name":"員工姓名",
                     "type":"string",
                     "value":"系統管理員",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "sendTime":{
                     "name":"寄發時間",
                     "type":"string",
                     "value":"0923",
                     "format":"HHmm",
                     "id":"sendTime"
                  },
                  "errorDate":{
                     "name":"異常日期",
                     "type":"string",
                     "value":"20220701",
                     "format":"YYYYmmdd",
                     "id":"errorDate"
                  },
                  "sendPersonnel":{
                     "name":"寄發員工本人",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"sendPersonnel"
                  },
                  "result":{
                     "name":"寄發結果",
                     "type":"string",
                     "value":"成功",
                     "format":"n/a",
                     "id":"result"
                  }
               },
               "format":"n/a",
               "id":"sendMailList"
            }
         ],
         "format":"n/a",
         "id":"sendMailList"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常，表示無通知紀錄
```json
{
    "status": "success",
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
