# appEmployeeCalendarQuery
取得員工個人行事曆特定事件詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appEmployeeCalendarQuery
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
| request | {eventNo:XXXXXXXXXXXXXX, empid:admin} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "eventNo":"XXXXXXXXXXXXXX", 
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
| eventNo | XXXXXXXXXXXXXX | String | 事件序號 | Y | n/a |
| empid | admin | String | 員工編號 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "employeeCalendar":{
         "id":"employeeCalendar",
         "name":"員工個人行事曆詳細資料",
         "value":[
            {
               "eventNo":{
                  "id":"eventNo",
                  "name":"行事曆編號",
                  "value":"XXXXXXXXXXXXXX",
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
               "eventBeginDate":{
                  "id":"eventBeginDate",
                  "name":"事件起始日期",
                  "value":"20211123",
                  "type":"string",
                  "format":"YYYYmmdd"
               },
               "eventEndDate":{
                  "id":"eventEndDate",
                  "name":"事件結束日期",
                  "value":"20211123",
                  "type":"string",
                  "format":"YYYYmmdd"
               },
               "isFullDayEvent":{
                  "id":"isFullDayEvent",
                  "name":"是否為全天候事件",
                  "value":true,
                  "type":"boolean",
                  "format":"n/a"
               },
               "eventBeginTime":{
                  "id":"eventBeginTime",
                  "name":"事件起始時間",
                  "value":"0900",
                  "type":"string",
                  "format":"HHmm"
               },
               "eventEndTime":{
                  "id":"eventEndTime",
                  "name":"事件結束時間",
                  "value":"1500",
                  "type":"string",
                  "format":"HHmm"
               },
               "eventSubject":{
                  "id":"eventSubject",
                  "name":"行事曆主旨",
                  "value":"HR APP會議",
                  "type":"string",
                  "format":"n/a"
               },
               "eventContent":{
                  "id":"eventContent",
                  "name":"行事曆內容",
                  "value":"今天要開會XXXX",
                  "type":"string",
                  "format":"n/a"
               },
               "eventLocation":{
                  "id":"eventLocation",
                  "name":"地點資訊",
                  "value":"英特內軟體",
                  "type":"string",
                  "format":"n/a"
               }
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":"",
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分"
         }
      }
   }
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
