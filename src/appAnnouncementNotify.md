# appAnnouncementNotify
取得未讀取通知數量

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAnnouncementNotify
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

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820"
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "announcementNotify":{
         "name":"通知資訊",
         "type":"object",
         "value":{
            "notifyCount":{
               "name":"通知未讀數量",
               "type":"integer",
               "value":0,
               "format":"count",
               "id":"notifyCount"
            }
         },
         "format":"n/a",
         "id":"announcementNotify"
      },
      "properties":{
         "format":{
            "count":"數量",
            "n/a":""
         }
      }
   }
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
