# appChatPersonalList
個人聊天室列表資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatPersonalList
```

### HTTP Request Method
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
    "properties": {
      "format": {
        "HHmm": "時間時分",
        "YYYYmmdd": "西元年月日",
        "count": "數量",
        "n/a": ""
      }
    },
    "personalList": {
      "name": "個人聊天室列表",
      "type": "array",
      "value": [
        {
          "name": "聊天室資訊",
          "type": "object",
          "value": {
            "unreadCount": {
              "name": "未讀數量",
              "type": "integer",
              "value": 24,
              "format": "count",
              "id": "unreadCount"
            },
            "sendTime": {
              "name": "發送時間",
              "type": "string",
              "value": "1900",
              "format": "HHmm",
              "id": "sendTime"
            },
            "partner": {
              "name": "聊天對象",
              "type": "object",
              "value": {
                "photo":{
                   "name":"員工照片",
                   "type":"string",
                   "value":"url",
                   "id":"photo"
                },
                "empFullName": {
                  "name": "員工中文姓名",
                  "type": "string",
                  "value": "報表一TEST1105",
                  "format": "n/a",
                  "id": "empFullName"
                },
                "employeeId": {
                  "name": "員工編號",
                  "type": "string",
                  "value": "00001",
                  "format": "n/a",
                  "id": "employeeId"
                }
              },
              "format": "n/a",
              "id": "partner"
            },
            "content": {
              "name": "訊息內容",
              "type": "string",
              "value": "錢",
              "format": "n/a",
              "id": "content"
            },
            "roomId": {
              "name": "聊天室鍵值",
              "type": "string",
              "value": "123456789",
              "format": "n/a",
              "id": "roomId"
            },
            "sendDate": {
              "name": "發送日期",
              "type": "string",
              "value": "20220915",
              "format": "YYYYmmdd",
              "id": "sendDate"
            },
            "textId": {
              "name": "訊息鍵值",
              "type": "string",
              "value": "1165",
              "format": "n/a",
              "id": "textId"
            }
          },
          "format": "n/a",
          "id": "chatRoom"
        }
      ],
      "format": "n/a",
      "id": "personalList"
    }
  }
}
```

### HTTP Response when No Data 
無資料則屬於正常現象
```json
{
    "status": "success",
    "message": [
        "查無資料"
    ],
    "data": {
        "personalList": {
            "name": "個人聊天室列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "personalList"
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
