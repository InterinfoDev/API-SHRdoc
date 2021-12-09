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
| request | {eventNo:uuid,empid:admin,eventBeginDate:20211101,eventEndDate:20211101,isFullDayEvent:false,eventBeginTime:0900,eventEndTime:1000,eventSubject:xxx,eventContent:xxx,eventLocation:interinfo} | Object | 查詢條件

### JSON representation Case 1 - Not Full Day Event  (Update)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "eventNo":"uuid",  --lucas 移除empid，應該從getUser來
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

### JSON representation Case 2 - Full Day Event (Update)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "eventNo":"uuid",  --lucas 移除empid，應該從getUser來
        "eventBeginDate":"20211101", 
        "eventEndDate":"20211101", 
        "isFullDayEvent":false, 
        "eventBeginTime":"",  --lucas 若為全天事件，起始時間空白
        "eventEndTime":"",    --lucas 若為全天事件，結束時間空白
        "eventSubject":"XXX", 
        "eventContent":"XXX", 
        "eventLocation":"interinfo", 
    }
}
```

### JSON representation Case 3 - Not Full Day Event  (Add)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{--lucas 移除empid，應該從getUser來
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

### JSON representation Case 4 - Full Day Event (Add)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{--lucas 移除empid，應該從getUser來
        "eventBeginDate":"20211101", 
        "eventEndDate":"20211101", 
        "isFullDayEvent":false, 
        "eventBeginTime":"",  --lucas 若為全天事件，起始時間空白
        "eventEndTime":"",    --lucas 若為全天事件，結束時間空白
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| eventNo | uuid | String | 行事曆單號 | N | UUID | 新增時不需傳入，修改時為必須傳入且不可空白 |
| eventBeginDate | 20211101 | String | 開始日期 | Y | AC(YYYYmmdd) |新增與修改時必須傳入 |
| eventEndDate | 20211101 | String | 結束日期 | Y | AC(YYYYmmdd) |新增與修改時必須傳入 |
| isFullDayEvent | true | boolean | 全天 | Y | n/a |新增與修改時必須傳入，若傳入為true，開始時間與結束時間必須為空白傳入，反之開始時間與結束時間不可空白 |
| eventBeginTime | 0900 | String | 開始時間 | Y | TIME(HHmm) |新增與修改時必須傳入，若全天候傳入為true，開始時間必須為空白傳入，反之不可空白 |
| eventEndTime | 1000 | String | 結束時間 | Y | TIME(HHmm) | 新增與修改時必須傳入，若全天候傳入為true，結束時間必須為空白傳入，反之不可空白 |
| eventSubject | XXX | String | 事件標題 | Y | n/a |新增與修改時必須傳入，但可空白 |
| eventContent | XXX | String | 內文 | Y | n/a |新增與修改時必須傳入，但可空白 |
| eventLocation | interinfo | String | 地點 | Y | n/a |新增與修改時必須傳入，但可空白 |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "calendar":{  --lucas改名
         "id":"calendar", --lucas改名
         "name":"異動員工個人行事曆",
         "value":{
            "executeResult":{
               "id":"executeResult",
               "name":"異動結果",
               "value":true,
               "type":"boolean",
               "format":"n/a"
            },
            "eventNo":{
               "id":"eventNo",
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

### HTTP Response when No Data 
若有傳入eventNo，不屬於登入者，無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
