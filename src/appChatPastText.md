# appChatPastText
往下滑取得舊的聊天紀錄

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatPastText
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
| date | 日期 |
| img | 圖片 |
| file | 檔案 |
| replyFile | 回覆檔案 |
| replyImg | 回覆圖片 |
| replyText | 回覆文字 |


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
               "name":"訊息資訊",
               "type":"object",
               "value":{
                  "reply":{
                      "name":"回覆資訊",
                      "type":"object",
                      "value":{
                         "sender":{
                            "name":"發送人員",
                            "type":"string",
                            "value":"",
                            "format":"n/a",
                            "id":"sender"
                         },
                         "textId":{
                            "name":"訊息鍵值",
                            "type":"string",
                            "value":"",
                            "format":"n/a",
                            "id":"textId"
                         },
                         "content":{
                            "name":"訊息內容",
                            "type":"string",
                            "value":"",
                            "format":"n/a",
                            "id":"content"
                         }
                      },
                      "format":"n/a",
                      "id":"reply"
                   },
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
                  "sender":{
                     "name":"發送人員",
                     "type":"string",
                     "value":"admin",
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
                     "value":"20230303121800605",
                     "format":"n/a",
                     "id":"timestamp"
                  },
                  "content":{
                     "name":"內容",
                     "type":"string",
                     "value":"2",
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
                     "value":"1218",
                     "format":"HHmm",
                     "id":"sendTime"
                  },
                  "sendDate":{
                     "name":"發送日期",
                     "type":"string",
                     "value":"20230303",
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
                     "value":"0c333dde-a83e-453e-9352-81a5177c1139",
                     "format":"n/a",
                     "id":"textId"
                  }
               },
               "format":"n/a",
               "id":"textInfo"
            },
            {
               "name":"訊息資訊",
               "type":"object",
               "value":{
                  "reply":{
                      "name":"回覆資訊",
                      "type":"object",
                      "value":{
                         "sender":{
                            "name":"發送人員",
                            "type":"string",
                            "value":"",
                            "format":"n/a",
                            "id":"sender"
                         },
                         "textId":{
                            "name":"訊息鍵值",
                            "type":"string",
                            "value":"",
                            "format":"n/a",
                            "id":"textId"
                         },
                         "content":{
                            "name":"訊息內容",
                            "type":"string",
                            "value":"",
                            "format":"n/a",
                            "id":"content"
                         }
                      },
                      "format":"n/a",
                      "id":"reply"
                   },
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
                  "sender":{
                     "name":"發送人員",
                     "type":"string",
                     "value":"admin",
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
                     "value":"20230303121728232",
                     "format":"n/a",
                     "id":"timestamp"
                  },
                  "content":{
                     "name":"內容",
                     "type":"string",
                     "value":"1",
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
                     "value":"1217",
                     "format":"HHmm",
                     "id":"sendTime"
                  },
                  "sendDate":{
                     "name":"發送日期",
                     "type":"string",
                     "value":"20230303",
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
                     "value":"3a38fe12-22e9-44e9-92f2-15923d43b514",
                     "format":"n/a",
                     "id":"textId"
                  }
               },
               "format":"n/a",
               "id":"textInfo"
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
