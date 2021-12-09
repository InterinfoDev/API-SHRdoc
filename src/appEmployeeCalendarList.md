# appEmployeeCalendarList
取得特定員工行事曆資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appEmployeeCalendarList
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
| request | {eventYM:202111, eventStartDate:20211101, eventEndDate:20211130, eventDate:20211130} | Object | 查詢條件

### JSON representation
Case 1 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 移除empid，改用getUser
        "eventStartDate":"20211101",
        "eventEndDate":"20211130"
    }
}
```
Case 2 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 移除empid，改用getUser
        "eventYM":"202111"
    }
}
```
Case 3 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 移除empid，改用getUser
        "eventDate":"20211101",
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
| Case No | Key | Value | Type | Description | Required | Format |
|:----------|:----------|:-------------|:-----|:------------|:------------|:------------|
| 1 | eventStartDate | 20211101 | String | 開始日期 | Y | AC(YYYYmmdd) |
|   | eventEndDate | 20211130 | String | 結束日期 | Y | AC(YYYYmmdd) |
| 2  | eventYM | 202111 | String | 年月 | Y | AC(YYYYmm) |
| 3  | eventDate | 20211130 | String | 日期 | Y | AC(YYYYmmdd) |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "employeeCalendarList":{
         "id":"employeeCalendarList",
         "name":"員工個人行事曆列表",
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
                  "name":"開始日期", --lucas改名
                  "value":"20211123",
                  "type":"string",
                  "format":"YYYYmmdd"
               },
               "eventEndDate":{
                  "id":"eventEndDate",
                  "name":"結束日期", --lucas改名
                  "value":"20211123",
                  "type":"string",
                  "format":"YYYYmmdd"
               },
               "isFullDayEvent":{
                  "id":"isFullDayEvent",
                  "name":"全天", --lucas改名
                  "value":true,
                  "type":"boolean",
                  "format":"n/a"
               },
               "eventBeginTime":{
                  "id":"eventBeginTime",
                  "name":"開始時間", --lucas改名
                  "value":"0900",
                  "type":"string",
                  "format":"HHmm"
               },
               "eventEndTime":{
                  "id":"eventEndTime",
                  "name":"結束時間", --lucas改名
                  "value":"1500",
                  "type":"string",
                  "format":"HHmm"
               },
               "eventSubject":{
                  "id":"eventSubject",
                  "name":"事件標題", --lucas改名
                  "value":"HR APP會議",
                  "type":"string",
                  "format":"n/a"
               },
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

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "employeeCalendarList":{
         "id":"employeeCalendarList",
         "name":"員工個人行事曆列表",
         "value":[],  --lucas 修改
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
