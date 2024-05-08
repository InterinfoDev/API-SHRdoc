# appChatGroupList
群組聊天室資料列表

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatGroupList
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
    "groupList": {
      "name": "群組聊天室列表",
      "type": "array",
      "value": [
        {
          "name": "聊天室資訊",
          "type": "object",
          "value": {
            "roomId": {
              "name": "聊天室鍵值",
              "type": "string",
              "value": "fb2d3320-1d83-4769-9643-3bdd5b960b80",
              "format": "n/a",
              "id": "roomId"
            },
            "groupMember": {
              "name": "群組成員",
              "type": "array",
              "value": [
                {
                  "name": "員工資訊",
                  "type": "object",
                  "value": {
                    "employeeId": {
                      "name": "員工編號",
                      "type": "string",
                      "value": "00001",
                      "format": "n/a",
                      "id": "employeeId"
                    },
                    "empFullName": {
                      "name": "員工中文姓名",
                      "type": "string",
                      "value": "報表一TEST1105",
                      "format": "n/a",
                      "id": "empFullName"
                    }
                  },
                  "format": "n/a",
                  "id": "employee"
                },
                {
                  "name": "員工資訊",
                  "type": "object",
                  "value": {
                    "employeeId": {
                      "name": "員工編號",
                      "type": "string",
                      "value": "00002",
                      "format": "n/a",
                      "id": "employeeId"
                    },
                    "empFullName": {
                      "name": "員工中文姓名",
                      "type": "string",
                      "value": "雙O菁",
                      "format": "n/a",
                      "id": "empFullName"
                    }
                  },
                  "format": "n/a",
                  "id": "employee"
                },
                {
                  "name": "員工資訊",
                  "type": "object",
                  "value": {
                    "employeeId": {
                      "name": "員工編號",
                      "type": "string",
                      "value": "admin",
                      "format": "n/a",
                      "id": "employeeId"
                    },
                    "empFullName": {
                      "name": "員工中文姓名",
                      "type": "string",
                      "value": "系統管理員",
                      "format": "n/a",
                      "id": "empFullName"
                    }
                  },
                  "format": "n/a",
                  "id": "employee"
                }
              ],
              "format": "n/a",
              "id": "groupMember"
            },
            "unreadCount": {
              "name": "未讀數量",
              "type": "integer",
              "value": 1,
              "format": "count",
              "id": "unreadCount"
            },
            "groupPhoto": {
              "name": "群組照片",
              "type": "string",
              "value": "url",
              "id": "groupPhoto"
            },
            "content": {
              "name": "訊息內容",
              "type": "string",
              "value": "感覺很豪吃",
              "format": "n/a",
              "id": "content"
            },
            "sendDate": {
              "name": "發送日期",
              "type": "string",
              "value": "20220831",
              "format": "YYYYmmdd",
              "id": "sendDate"
            },
            "sendTime": {
              "name": "發送時間",
              "type": "string",
              "value": "1607",
              "format": "HHmm",
              "id": "sendTime"
            },
            "textId": {
              "name": "訊息鍵值",
              "type": "string",
              "value": "0005",
              "format": "n/a",
              "id": "textId"
            },
            "groupName": {
              "name": "群組名稱",
              "type": "string",
              "value": "群組名稱",
              "format": "n/a",
              "id": "groupName"
            }
          },
          "format": "n/a",
          "id": "chatRoom"
        }
      ],
      "format": "n/a",
      "id": "groupList"
    },
    "properties": {
      "format": {
        "HHmm": "時間時分",
        "YYYYmmdd": "西元年月日",
        "hyperlink":"超連結",
        "count": "數量",
        "n/a": ""
      }
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
        "groupList": {
            "name": "群組聊天室列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "groupList"
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
