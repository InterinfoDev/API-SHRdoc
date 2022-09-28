# appChatRoom
獲取該聊天室相關資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatRoom
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
| request | {'roomId':'xxx'} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "roomId":"xxx"
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
| roomId | xxx | String | 聊天室鍵值 | Y | n/a |



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
            "n/a":""
         }
      },
      "chatRoom":{
         "name":"聊天室資訊",
         "type":"object",
         "value":{
            "roomName":{
               "name":"聊天室名稱",
               "type":"string",
               "value":"弓O漩NEW0036",
               "format":"n/a",
               "id":"roomName"
            },
            "roomType":{
               "name":"聊天室類型",
               "type":"string",
               "value":"personal",
               "format":"n/a",
               "id":"roomType"
            },
            "roomMember":{
               "name":"聊天室成員",
               "type":"array",
               "value":[
                  {
                     "name":"員工資訊",
                     "type":"object",
                     "value":{
                        "empFullName":{
                           "name":"員工中文姓名",
                           "type":"string",
                           "value":"弓O漩",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "roomMember":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"0036",
                           "format":"n/a",
                           "id":"empid"
                        }
                     },
                     "format":"n/a",
                     "id":"employee"
                  },
                  {
                     "name":"員工資訊",
                     "type":"object",
                     "value":{
                        "empFullName":{
                           "name":"員工中文姓名",
                           "type":"string",
                           "value":"連O慈",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "roomMember":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"0039",
                           "format":"n/a",
                           "id":"empid"
                        }
                     },
                     "format":"n/a",
                     "id":"employee"
                  }
               ],
               "format":"n/a",
               "id":"roomMember"
            },
            "roomId":{
               "name":"聊天室鍵值",
               "type":"string",
               "value":"6003d01f-55a5-4e25-b9e8-39060f1765d1",
               "format":"n/a",
               "id":"roomId"
            }
         },
         "format":"n/a",
         "id":"chatRoom"
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
