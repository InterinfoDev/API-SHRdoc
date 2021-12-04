# appEditEmployeeCalendar
異動員工個人行事曆

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appEditEmployeeCalendar
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
| request | {seriesNo:uuid,empid:admin,eventBeginDate:20211101,eventEndDate:20211101,isFullDayEvent:false,eventBeginTime:0900,eventEndTime:1000,eventSubject:xxx,eventContent:xxx,eventLocation:interinfo} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "seriesNo":"uuid", 
        "empid":"admin",
        "eventBeginDate":"20211101", 
        "eventEndDate":"20211101", 
        "isFullDayEvent":false, 
        "eventBeginTime":"0900", 
        "eventEndTime":"1000", 
        "eventSubject":"XXX", 
        "eventContent":"XXX", 
        "eventLocation":"interinfo", 
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
| seriesNo | uuid | String | 行事曆單號 | Y | UUID |
| empid | admin | String | 員工編號 | Y | n/a |
| eventBeginDate | 20211101 | String | 事件起始日期 | Y | AC(YYYYmmdd) |
| eventEndDate | 20211101 | String | 事件結束日期 | Y | AC(YYYYmmdd) |
| isFullDayEvent | true | boolean | 是否全天事件 | Y | n/a |
| eventBeginTime | 0900 | String | 起始時間 | Y | TIME(HHmm) |
| eventEndTime | 1000 | String | 結束時間 | Y | TIME(HHmm) |
| eventSubject | XXX | String | 事件標題 | Y | n/a |
| eventContent | XXX | String | 事件內容 | Y | n/a |
| eventLocation | interinfo | String | 地點 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "calendarInfo":{
         "id":"calendarInfo",
         "name":"異動員工個人行事曆",
         "value":{
            "executeResult":{
               "id":"executeResult",
               "name":"異動結果",
               "value":true,
               "type":"boolean",
               "format":"n/a"
            },
            "seriesNo":{
               "id":"seriesNo",
               "name":"行事曆編號",
               "value":"XXXXXXXXXXXXXX",
               "type":"string",
               "format":"n/a"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":""
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