# appChatTextReader
取得訊息讀取資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatTextReader
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
| request | {"roomId":"xxx", "textId":"xxx"} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{"roomId":"xxx", "textId":"xxx"}
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
| roomId | xxx | String | 聊天室ID | Y | n/a |
| textId | xxx | String | 訊息ID | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "textReadInfo":{
         "name":"訊息讀取資訊",
         "type":"object",
         "value":{
            "reader":{
               "name":"已讀人員",
               "type":"array",
               "value":[
                  {
                     "name":"個人資訊",
                     "type":"object",
                     "value":{
                        "empFullName":{
                           "name":"員工中文姓名",
                           "type":"string",
                           "value":"弓O倫",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "employeeId":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"0006",
                           "format":"n/a",
                           "id":"employeeId"
                        },
                        "photo":{
                           "name":"員工相片",
                           "type":"string",
                           "value":"url",
                           "format":"hyperlink",
                           "id":"photo"
                        },
                        "empFullEname":{
                           "name":"員工英文姓名",
                           "type":"string",
                           "value":"Kevin",
                           "format":"n/a",
                           "id":"empFullEname"
                        }
                     },
                     "format":"n/a",
                     "id":"employee"
                  }
               ],
               "format":"n/a",
               "id":"reader"
            },
            "unReader":{
               "name":"未讀人員",
               "type":"array",
               "value":[
                  {
                     "name":"個人資訊",
                     "type":"object",
                     "value":{
                        "empFullName":{
                           "name":"員工中文姓名",
                           "type":"string",
                           "value":"弓O佑",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "employeeId":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"1102",
                           "format":"n/a",
                           "id":"employeeId"
                        },
                        "photo":{
                           "name":"員工相片",
                           "type":"string",
                           "value":"url",
                           "format":"hyperlink",
                           "id":"photo"
                        },
                        "empFullEname":{
                           "name":"員工英文姓名",
                           "type":"string",
                           "value":"Kevin",
                           "format":"n/a",
                           "id":"empFullEname"
                        }
                     },
                     "format":"n/a",
                     "id":"employee"
                  }
               ],
               "format":"n/a",
               "id":"unReader"
            }
         },
         "format":"n/a",
         "id":"textReadInfo"
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
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
