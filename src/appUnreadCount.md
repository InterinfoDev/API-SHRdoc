# appUnreadCount
聊天室未讀訊息(群組+個人)

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appUnreadCount
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
    "right":"51341911904173543336756162544864820",
   }
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
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "unreadInfo": {
      "name": "未讀數量",
      "type": "object",
      "value": {
        "unreadCount": {
          "name": "未讀數量",
          "type": "integer",
          "value": 25,
          "format": "count",
          "id": "unreadCount"
        },
        "haveUnreadText": {
          "name": "是否有未讀訊息",
          "type": "boolean",
          "value": true,
          "format": "n/a",
          "id": "haveUnreadText"
        }
      },
      "format": "n/a",
      "id": "unreadInfo"
    },
    "properties": {
      "format": {
        "count": "數量",
        "n/a": ""
      }
    }
  }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤
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
