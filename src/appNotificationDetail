# appNotificationDetail
取得推播詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appNotificationDetail
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {notificationKey:5497D73A-8178-49E5-9073-CDAA25889B20} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "notificationKey":"5497D73A-8178-49E5-9073-CDAA25889B20", 
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
| attendYM | 202104 | String | 考勤年月 | Y | AC(YYYYmm) |
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
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "notification":{
         "name":"公告詳細資料",
         "type":"object",
         "value":{
            "read":{
               "name":"是否已讀推播",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"read"
            },
            "notificationKey":{
               "name":"推播編號",
               "type":"string",
               "value":"83568E9F-56B7-41C7-956C-395ACE99FAC1",
               "format":"n/a",
               "id":"notificationKey"
            },
            "FunctionName":{
               "name":"功能名稱",
               "type":"string",
               "value":"測試功能",
               "format":"n/a",
               "id":"FunctionName"
            },
            "notificationType":{
               "name":"推播種類",
               "type":"string",
               "value":"簽核",
               "format":"n/a",
               "id":"notificationType"
            },
            "content":{
               "name":"推播內容",
               "type":"string",
               "value":"測試內容",
               "format":"n/a",
               "id":"content"
            },
            "title":{
               "name":"推播標題",
               "type":"string",
               "value":"測試標頭",
               "format":"n/a",
               "id":"title"
            },
            "sendDate":{
               "name":"發送日期",
               "type":"string",
               "value":"20220426",
               "format":"YYYYmmdd",
               "id":"sendDate"
            },
            "sendTime":{
               "name":"發送時間",
               "type":"string",
               "value":"1535",
               "format":"HHmm",
               "id":"sendTime"
            },
            "pkgName":{
               "name":"使用PKG",
               "type":"string",
               "value":"hrm8w.pkg",
               "format":"n/a",
               "id":"pkgName"
            }
         },
         "format":"n/a",
         "id":"notification"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
