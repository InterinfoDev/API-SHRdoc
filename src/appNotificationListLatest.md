# appNotificationListLatest
查詢推播清單最新資訊(全部)
2024/03/22 查詢上拉給予全部最新 不限制筆數

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appNotificationListLatest
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
| request | {notificationKey:0BB562CB-E166-4D69-9C50-C0EDF2511A38, notificationType:all} | Object | 查詢條件

### JSON representation
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "notificationKey":"5497D73A-8178-49E5-9073-CDAA25889B20",
        "notificationType":"all"
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
 Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| notificationKey | 5497D73A-8178-49E5-9073-CDAA25889B20 | String | 推播最新一筆通知ID | N | n/a |
| notificationType | all | String | 查詢通知類別 | Y | 全部:all , 簽核:flow , 訊息:hr , 系統:sys |

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
   "isLast":{
         "name":"是否為最後一筆通知",
         "type":"boolean",
         "value":true,
         "format":"n/a",
         "id":"isLast"
     },
      "notificationList":{
         "name":"推播列表",
         "type":"array",
         "value":[
            {
               "name":"推播資訊",
               "type":"object",
               "value":{
                  "sendTime":{
                     "name":"發送時間",
                     "type":"string",
                     "value":"1535",
                     "format":"HHmm",
                     "id":"sendTime"
                  },
                  "content":{
                     "name":"推播內容",
                     "type":"string",
                     "value":"測試內容",
                     "format":"n/a",
                     "id":"content"
                  },
                  "read":{
                     "name":"是否已讀推播",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"read"
                  },
                  "sendDate":{
                     "name":"發送日期",
                     "type":"string",
                     "value":"20220426",
                     "format":"YYYYmmdd",
                     "id":"sendDate"
                  },
                  "notificationKey":{
                     "name":"推播編號",
                     "type":"string",
                     "value":"83568E9F-56B7-41C7-956C-395ACE99FAC1",
                     "format":"n/a",
                     "id":"notificationKey"
                  },
                  "notificationType":{
                     "name":"推播種類",
                     "type":"string",
                     "value":"B",
                     "format":"n/a",
                     "id":"notificationType"
                  },
                  "title":{
                     "name":"推播標題",
                     "type":"string",
                     "value":"測試標頭",
                     "format":"n/a",
                     "id":"title"
                  },
                  "passTime": {
                     "name": "經過時間",
                     "type": "string",
                     "value": "1天前",
                     "format": "n/a",
                     "id": "passTime"
                  }
               },
               "format":"n/a",
               "id":"notification"
            }
         ],
         "format":"n/a",
         "id":"notificationList"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常情況
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        },
        "notificationList": {
            "name": "通知列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "notificationList"
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
