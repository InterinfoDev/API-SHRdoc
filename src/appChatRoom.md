# appChatRoom
點及聊天室獲取該聊天室相關資料

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
| request | {'roomId':'xxx', 'haveUnReadText':false} | Object | 查詢條件

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
| haveUnReadText | false | boolean | 是否有未讀訊息 | Y | n/a |



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
            "base64":"Base64編碼格式",
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "hyperlink":"超連結"
         }
      },
      "chatRoom":{
         "name":"聊天室資訊",
         "type":"object",
         "value":{
            "roomName":{
               "name":"聊天室名稱",
               "type":"string",
               "value":"測試",
               "format":"n/a",
               "id":"roomName"
            },
            "roomType":{
               "name":"聊天室類型",
               "type":"string",
               "value":"group",
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
                           "value":"何O以",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "employeeId":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"0018",
                           "format":"n/a",
                           "id":"employeeId"
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
                           "value":"解O庭",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "employeeId":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"0222",
                           "format":"n/a",
                           "id":"employeeId"
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
               "value":"9de123a0-1077-4716-bbda-ce91e42ed674",
               "format":"n/a",
               "id":"roomId"
            }
         },
         "format":"n/a",
         "id":"chatRoom"
      },
      "textRecord":{
         "name":"聊天紀錄",
         "type":"array",
         "value":[
            {
               "name":"20230220(一)",
               "type":"array",
               "value":[
                  {
                     "name":"訊息資訊",
                     "type":"object",
                     "value":{
                        "file":{
                           "name":"檔案資訊",
                           "type":"object",
                           "value":{
                              "fileType":{
                                 "name":"檔案類型",
                                 "type":"string",
                                 "value":"",
                                 "format":"n/a",
                                 "id":"fileType"
                              },
                              "fileUrl":{
                                 "name":"檔案路徑",
                                 "type":"string",
                                 "value":"",
                                 "format":"n/a",
                                 "id":"fileUrl"
                              },
                              "fileName":{
                                 "name":"檔案名稱",
                                 "type":"string",
                                 "value":"",
                                 "format":"n/a",
                                 "id":"fileName"
                              }
                           },
                           "format":"n/a",
                           "id":"file"
                        },
                        "isFirst":{
                           "name":"是否為當日第一筆訊息",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"isFirst"
                        },
                        "sender":{
                           "name":"發送人員",
                           "type":"string",
                           "value":"0018",
                           "format":"n/a",
                           "id":"sender"
                        },
                        "reader":{
                           "name":"已讀人員",
                           "type":"array",
                           "value":[
                              
                           ],
                           "format":"n/a",
                           "id":"reader"
                        },
                        "timestamp":{
                           "name":"時間戳",
                           "type":"string",
                           "value":"20230220141803406",
                           "format":"n/a",
                           "id":"timestamp"
                        },
                        "content":{
                           "name":"內容",
                           "type":"string",
                           "value":"Fff",
                           "format":"n/a",
                           "id":"content"
                        },
                        "isRead":{
                           "name":"是否已讀",
                           "type":"boolean",
                           "value":false,
                           "format":"n/a",
                           "id":"isRead"
                        },
                        "textType":{
                           "name":"訊息類型",
                           "type":"string",
                           "value":"text",
                           "format":"n/a",
                           "id":"textType"
                        },
                        "sendTime":{
                           "name":"發送時間",
                           "type":"string",
                           "value":"1418",
                           "format":"HHmm",
                           "id":"sendTime"
                        },
                        "sendDate":{
                           "name":"發送日期",
                           "type":"string",
                           "value":"20230220",
                           "format":"YYYYmmdd",
                           "id":"sendDate"
                        },
                        "isLoginId":{
                           "name":"是否為登入者",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"isLoginId"
                        },
                        "readCount":{
                           "name":"已讀數量",
                           "type":"integer",
                           "value":0,
                           "format":"count",
                           "id":"readCount"
                        },
                        "textId":{
                           "name":"訊息鍵值",
                           "type":"string",
                           "value":"C3663FAF-CD4F-4EAF-B17B-7869C7F12456",
                           "format":"n/a",
                           "id":"textId"
                        }
                     },
                     "format":"n/a",
                     "id":"textInfo"
                  }
               ],
               "format":"n/a",
               "id":"20230220"
            }
         ],
         "format":"n/a",
         "id":"textRecord"
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
