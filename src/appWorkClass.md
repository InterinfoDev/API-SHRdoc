# appWorkClass
取得查詢當天班別資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appWorkClass
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
| request | {empid:admin , date:20220214} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin", 
        "date":"20220214",
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
| empid | admin | String | 員工編號 | Y | n/a |
| date | 20220214 | String | 查詢日期 | Y | AC(YYYYmmdd) |

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
            "HHmm":"時間時分"
         }
      },
      "class":{
         "name":"班別資訊",
         "type":{
            "workOff":{
               "name":"下班時間",
               "type":"1700",
               "format":"object",
               "id":"workOff"
            },
            "workOn":{
               "name":"上班時間",
               "type":"0800",
               "format":"object",
               "id":"workOn"
            },
            "workClassName":{
               "name":"班別名稱",
               "type":"通用中和0800",
               "format":"object",
               "id":"workClassName"
            },
            "workDate":{
               "name":"班別日期",
               "type":"20220214",
               "format":"object",
               "id":"workDate"
            },
            "workClass":{
               "name":"班別代號",
               "type":"00",
               "format":"object",
               "id":"workClass"
            }
         },
         "format":"object",
         "id":"class"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於資料異常，不太可能沒有下拉選項
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
