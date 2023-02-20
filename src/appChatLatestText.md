# appChatLatestText
往上滑取得新的聊天紀錄

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatLatestText
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
| request | {'roomId':'123456789','textId':'xxx'} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "roomId":"123456789",
        "textId":"xxx"
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
| roomId | 123456789 | String | 員工編號 | Y | n/a |
| textId | xxx | String | 取得最後一筆訊息的KEY | Y | n/a |

### TextType
| textType | Description |
|:---------|:------------|
| text | 一般訊息 |
| sysText | 系統訊息 |
| img | 圖片 |
| file | 檔案 |


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
      "textRecord":{
         "name":"聊天紀錄",
         "type":"array",
         "value":[
            {
               "name":"20220901(四)",
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
                        "reader":{
                           "name": "已讀人員",
                           "type": "array",
                           "value": [
                               "00002"
                           ],
                           "format": "n/a",
                           "id": "reader"
                        },
                        "timestamp":{
                           "name":"時間戳",
                           "type":"string",
                           "value":"20230220115252771",
                           "format":"n/a",
                           "id":"timestamp"
                        },
                        "sender":{
                           "name":"發送人員",
                           "type":"string",
                           "value":"admin",
                           "format":"n/a",
                           "id":"sender"
                        },
                        "content":{
                           "name":"內容",
                           "type":"string",
                           "value": "url",
                           "id":"content"
                        },
                        "isRead":{
                           "name":"是否已讀",
                           "type":"boolean",
                           "value":false,
                           "format":"n/a",
                           "id":"isRead"
                        },
                        "isFirst":{
                           "name":"是否為當日第一筆訊息",
                           "type":"boolean",
                           "value":false,
                           "format":"n/a",
                           "id":"isFirst"
                        },
                        "textType":{
                           "name":"訊息類型",
                           "type":"string",
                           "value":"img",
                           "format":"n/a",
                           "id":"textType"
                        },
                        "sendTime":{
                           "name":"發送時間",
                           "type":"string",
                           "value":"1023",
                           "format":"HHmm",
                           "id":"sendTime"
                        },
                        "sendDate":{
                           "name":"發送日期",
                           "type":"string",
                           "value":"20220901",
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
                           "value":"1115",
                           "format":"n/a",
                           "id":"textId"
                        }
                     },
                     "format":"n/a",
                     "id":"textInfo"
                  }
               ],
               "format":"n/a",
               "id":"20220901"
            },
            {
               "name":"20220831(三)",
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
                        "reader":{
                           "name": "已讀人員",
                           "type": "array",
                           "value": [
                               "00002"
                           ],
                           "format": "n/a",
                           "id": "reader"
                        },
                        "timestamp":{
                           "name":"時間戳",
                           "type":"string",
                           "value":"20230220115252771",
                           "format":"n/a",
                           "id":"timestamp"
                        },
                        "sender":{
                           "name":"發送人員",
                           "type":"string",
                           "value":"admin",
                           "format":"n/a",
                           "id":"sender"
                        },
                        "content":{
                           "name":"內容",
                           "type":"string",
                           "value":"吃噗噗",
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
                        "isFirst":{
                           "name":"是否為當日第一筆訊息",
                           "type":"boolean",
                           "value":false,
                           "format":"n/a",
                           "id":"isFirst"
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
                           "value":"1607",
                           "format":"HHmm",
                           "id":"sendTime"
                        },
                        "sendDate":{
                           "name":"發送日期",
                           "type":"string",
                           "value":"20220831",
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
                           "value":"1114",
                           "format":"n/a",
                           "id":"textId"
                        }
                     },
                     "format":"n/a",
                     "id":"textInfo"
                  }
               ],
               "format":"n/a",
               "id":"20220831"
            }
         ],
         "format":"n/a",
         "id":"textRecord"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於正常範圍
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "properties": {
            "format": {
                "base64": "Base64編碼格式",
                "YYYYmmdd": "西元年月日",
                "n/a": "",
                "hyperlink": "超連結"
            }
        },
        "textRecord": {
            "name": "聊天紀錄",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "textRecord"
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
