# appOvertimeList
查詢單一員工該年月區間的實際加班資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeList
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
| request | {overtimeYM:202201, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的員工及畫面上的年月取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "overtimeYM":"202201", 
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
| overtimeYM | 202201 | String | 查詢年月 | Y | AC(YYYYmm) |
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
         "name":"個人實際加班",
         "type":"object",
         "value":{
            "overtimeYM":{
               "name":"實際加班年月",
               "type":"string",
               "value":"202201",
               "format":"YYYYmm",
               "id":"overtimeYM"
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
               "value":"L1線B班",
               "format":"n/a",
               "id":"depFullName"
            }
         },
         "format":"n/a",
         "id":"employee"
      },
      "overtimeList":{
         "name":"個人實際加班列表",
         "type":"array",
         "value":[
            {
               "name":"實際加班資訊",
               "type":"object",
               "value":{
                  "amt":{
                     "name":"總計",
                     "type":"decimal",
                     "value":12.0,
                     "format":"hour",
                     "id":"amt"
                  },
                  "startTime":{            --richard 欄位修改  startTime
                     "name":"起始時間",
                     "type":"string",
                     "value":"0800",
                     "format":"HHmm",
                     "id":"startTime"       --richard 欄位修改  startTime
                  },
                  "startDate":{              --richard 欄位修改  startDate
                     "name":"起始日期",
                     "type":"string",
                     "value":"20220108",
                     "format":"YYYYmmdd",
                     "id":"startDate"         --richard 欄位修改  startDate
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "pno":{
                     "name":"實際加班單號",
                     "type":"string",
                     "value":"H002022031100001",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "payTypeName":{
                     "name":"給付方式名稱",
                     "type":"string",
                     "value":"給薪",
                     "format":"n/a",
                     "id":"payTypeName"
                  },
                  "endTime":{               --richard 欄位修改  endTime
                     "name":"結束時間",
                     "type":"string",
                     "value":"1700",
                     "format":"HHmm",
                     "id":"endTime"         --richard 欄位修改  endTime
                  },
                  "endDate": {
                     "name": "結束日期",
                     "type": "string",
                     "value": "20220108",
                     "format": "YYYYmmdd",
                     "id": "endDate"
                  },
                  "overplanPno":{
                     "name":"預定加班單號",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"overplanPno"
                  },
                  "overtimeType": {         --richard 新增欄位 overtimeType
                    "name": "加班種類",
                    "type": "string",
                    "value": "一般加班",
                    "format": "n/a",
                    "id": "overtimeType"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"overtime"
            },
            {
               "name":"實際加班資訊",
               "type":"object",
               "value":{
                  "amt":{
                     "name":"總計",
                     "type":"decimal",
                     "value":8.0,
                     "format":"hour",
                     "id":"amt"
                  },
                  "startTime":{
                     "name":"起始時間",
                     "type":"string",
                     "value":"0800",
                     "format":"HHmm",
                     "id":"startTime"
                  },
                  "startDate":{
                     "name":"起始日期",
                     "type":"string",
                     "value":"20220101",
                     "format":"YYYYmmdd",
                     "id":"startDate"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "pno":{
                     "name":"實際加班單號",
                     "type":"string",
                     "value":"H002022031100002",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "payTypeName":{
                     "name":"給付方式名稱",
                     "type":"string",
                     "value":"給薪",
                     "format":"n/a",
                     "id":"payTypeName"
                  },
                  "endTime":{
                     "name":"結束時間",
                     "type":"string",
                     "value":"1600",
                     "format":"HHmm",
                     "id":"endTime"
                  },
                  "overplanPno":{
                     "name":"預定加班單號",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"overplanPno"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"overtime"
            },
            {
               "name":"實際加班資訊",
               "type":"object",
               "value":{
                  "amt":{
                     "name":"總計",
                     "type":"decimal",
                     "value":4.0,
                     "format":"hour",
                     "id":"amt"
                  },
                  "startTime":{
                     "name":"起始時間",
                     "type":"string",
                     "value":"1700",
                     "format":"HHmm",
                     "id":"startTime"
                  },
                  "startDate":{
                     "name":"起始日期",
                     "type":"string",
                     "value":"20220105",
                     "format":"YYYYmmdd",
                     "id":"startDate"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "pno":{
                     "name":"實際加班單號",
                     "type":"string",
                     "value":"H002022031100003",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "payTypeName":{
                     "name":"給付方式名稱",
                     "type":"string",
                     "value":"給薪",
                     "format":"n/a",
                     "id":"payTypeName"
                  },
                  "endTime":{
                     "name":"結束時間",
                     "type":"string",
                     "value":"2100",
                     "format":"HHmm",
                     "id":"endTime"
                  },
                  "overplanPno":{
                     "name":"預定加班單號",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"overplanPno"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"overtime"
            }
         ],
         "format":"n/a",
         "id":"overtimeList"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "YYYYmm":"西元年月"
         }
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
