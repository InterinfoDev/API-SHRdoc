# appCreateGroupChatRoom
創建群組聊天室

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appCreateGroupChatRoom
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
| request | {'groupName':'xxx', 'empid':['xxx'], 'groupPhoto':{'fileName':'xxx', 'fileData':'base64'}} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
      "groupName":"xxx", 
      "empid":["admin"],
      "groupPhoto":{
        "fileName":"kevin.jpg",
        "fileData":"base64"
      }
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
| groupName | xxx | String | 群組名稱 | Y | n/a |
| empid | xxx | String | 群組人員 | Y | n/a |
| groupPhoto |  | String | 群組圖片 |  | n/a |
| fileName | test.jpg | String | 群組圖片 | Y | n/a |
| fileData |  | String | 群組圖片 | Y | base64 |



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
            "roomType":{
               "name":"聊天室類型",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"roomType"
            },
            "roomName":{    --kevin新增roomName
               "name":"聊天室名稱",
               "type":"string",
               "value":"xxx",
               "format":"n/a",
               "id":"roomName"
            },
            "roomMember":{
               "name":"聊天室成員",
               "type":"string",
               "value":[
                  {
                     "name":"員工編號",
                     "type":"string",
                     "value":"00001",
                     "format":"n/a",
                     "id":"employeeId"
                  },
                  {
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"employeeId"
                  }
               ],
               "format":"n/a",
               "id":"roomMember"
            },
            "roomId":{
               "name":"聊天室鍵值",
               "type":"string",
               "value":"123456789",
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
