# appCreatePersonalChatRoom
創建個人聊天室，或從夥伴查詢進入也是使用此API

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appCreatePersonalChatRoom
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
| request | {'employeeId':'10002047'} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "employeeId":"10002047"
    }
}
```
### textType
| key | Description |
|:---------|:------------|
| text | 一般文字 |
| img | 圖片 |
| hyperlink | 超連結 |
| file | 檔案 |
| sysText | 系統訊息 |


### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |


### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| employeeId | 10002047 | String | 員工編號 | Y | n/a |



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
                "base64": "Base64編碼格式",
                "YYYYmmdd": "西元年月日",
                "n/a": "",
                "hyperlink": "超連結"
            }
        },
        "chatRoom": {
            "name": "聊天室資訊",
            "type": "object",
            "value": {
                "roomType": {
                    "name": "聊天室類型",
                    "type": "string",
                    "value": "個人聊天室",
                    "format": "n/a",
                    "id": "roomType"
                },
                "roomMember": {
                    "name": "聊天室成員",
                    "type": "string",
                    "value": [
                        {
                            "name": "員工編號",
                            "type": "string",
                            "value": "10002047",
                            "format": "n/a",
                            "id": "employeeId"
                        },
                        {
                            "name": "員工編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "employeeId"
                        }
                    ],
                    "format": "n/a",
                    "id": "roomMember"
                },
                "roomId": {
                    "name": "聊天室鍵值",
                    "type": "string",
                    "value": "123456789",
                    "format": "n/a",
                    "id": "roomId"
                }
            },
            "format": "n/a",
            "id": "chatRoom"
        },
        "textRecord": {
            "name": "聊天紀錄",
            "type": "array",
            "value": [
                {
                    "name": "20220831(三)",
                    "type": "array",
                    "value": [
                        {
                            "name": "訊息資訊",
                            "type": "object",
                            "value": {
                                "file": {
                                    "name": "檔案資訊",
                                    "type": "object",
                                    "value": {
                                        "fileType": {
                                            "name": "檔案類型",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileType"
                                        },
                                        "fileUrl": {
                                            "name": "檔案路徑",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileUrl"
                                        },
                                        "fileName": {
                                            "name": "檔案名稱",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileName"
                                        }
                                    },
                                    "format": "n/a",
                                    "id": "file"
                                },
                                "sender": {
                                    "name": "發送人員",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "sender"
                                },
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "吃噗噗",
                                    "format": "n/a",
                                    "id": "content"
                                },
                                "isRead": {
                                    "name": "是否已讀",
                                    "type": "boolean",
                                    "value": false,
                                    "format": "n/a",
                                    "id": "isRead"
                                },
                                "textType": {
                                    "name": "訊息類型",
                                    "type": "string",
                                    "value": "text",
                                    "format": "n/a",
                                    "id": "textType"
                                },
                                "sendTime": {
                                    "name": "發送時間",
                                    "type": "string",
                                    "value": "1607",
                                    "format": "HHmm",
                                    "id": "sendTime"
                                },
                                "sendDate": {
                                    "name": "發送日期",
                                    "type": "string",
                                    "value": "20220831",
                                    "format": "YYYYmmdd",
                                    "id": "sendDate"
                                },
                                "isLoginId": {  --由此判斷訊息是顯示在左邊還是右邊
                                    "name": "是否為登入者",
                                    "type": "boolean",
                                    "value": true,
                                    "format": "n/a",
                                    "id": "isLoginId"
                                },
                                "textId": {
                                    "name": "訊息鍵值",
                                    "type": "string",
                                    "value": "1114",
                                    "format": "n/a",
                                    "id": "textId"
                                }
                            },
                            "format": "n/a",
                            "id": "textInfo"
                        },
                        {
                            "name": "訊息資訊",
                            "type": "object",
                            "value": {
                                "file": {
                                    "name": "檔案資訊",
                                    "type": "object",
                                    "value": {
                                        "fileType": {
                                            "name": "檔案類型",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileType"
                                        },
                                        "fileUrl": {
                                            "name": "檔案路徑",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileUrl"
                                        },
                                        "fileName": {
                                            "name": "檔案名稱",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileName"
                                        }
                                    },
                                    "format": "n/a",
                                    "id": "file"
                                },
                                "roomId": {
                                    "name": "聊天室鍵值",
                                    "type": "string",
                                    "value": "123456789",
                                    "format": "n/a",
                                    "id": "roomId"
                                },
                                "sender": {
                                    "name": "發送人員",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "sender"
                                },
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "很好喔",
                                    "format": "n/a",
                                    "id": "content"
                                },
                                "isRead": {
                                    "name": "是否已讀",
                                    "type": "boolean",
                                    "value": false,
                                    "format": "n/a",
                                    "id": "isRead"
                                },
                                "textType": {
                                    "name": "訊息類型",
                                    "type": "string",
                                    "value": "text",
                                    "format": "n/a",
                                    "id": "textType"
                                },
                                "sendTime": {
                                    "name": "發送時間",
                                    "type": "string",
                                    "value": "1607",
                                    "format": "HHmm",
                                    "id": "sendTime"
                                },
                                "sendDate": {
                                    "name": "發送日期",
                                    "type": "string",
                                    "value": "20220831",
                                    "format": "YYYYmmdd",
                                    "id": "sendDate"
                                },
                                "isLoginId": {
                                    "name": "是否為登入者",
                                    "type": "boolean",
                                    "value": true,
                                    "format": "n/a",
                                    "id": "isLoginId"
                                },
                                "textId": {
                                    "name": "訊息鍵值",
                                    "type": "string",
                                    "value": "1113",
                                    "format": "n/a",
                                    "id": "textId"
                                }
                            },
                            "format": "n/a",
                            "id": "textInfo"
                        },
                        {
                            "name": "訊息資訊",
                            "type": "object",
                            "value": {
                                "file": {
                                    "name": "檔案資訊",
                                    "type": "object",
                                    "value": {
                                        "fileType": {
                                            "name": "檔案類型",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileType"
                                        },
                                        "fileUrl": {
                                            "name": "檔案路徑",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileUrl"
                                        },
                                        "fileName": {
                                            "name": "檔案名稱",
                                            "type": "string",
                                            "value": "",
                                            "format": "n/a",
                                            "id": "fileName"
                                        }
                                    },
                                    "format": "n/a",
                                    "id": "file"
                                },
                                "roomId": {
                                    "name": "聊天室鍵值",
                                    "type": "string",
                                    "value": "123456789",
                                    "format": "n/a",
                                    "id": "roomId"
                                },
                                "sender": {
                                    "name": "發送人員",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "sender"
                                },
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "哈囉你好嗎",
                                    "format": "n/a",
                                    "id": "content"
                                },
                                "isRead": {
                                    "name": "是否已讀",
                                    "type": "boolean",
                                    "value": false,
                                    "format": "n/a",
                                    "id": "isRead"
                                },
                                "textType": {
                                    "name": "訊息類型",
                                    "type": "string",
                                    "value": "text",
                                    "format": "n/a",
                                    "id": "textType"
                                },
                                "sendTime": {
                                    "name": "發送時間",
                                    "type": "string",
                                    "value": "1607",
                                    "format": "HHmm",
                                    "id": "sendTime"
                                },
                                "sendDate": {
                                    "name": "發送日期",
                                    "type": "string",
                                    "value": "20220831",
                                    "format": "YYYYmmdd",
                                    "id": "sendDate"
                                },
                                "isLoginId": {
                                    "name": "是否為登入者",
                                    "type": "boolean",
                                    "value": true,
                                    "format": "n/a",
                                    "id": "isLoginId"
                                },
                                "textId": {
                                    "name": "訊息鍵值",
                                    "type": "string",
                                    "value": "1112",
                                    "format": "n/a",
                                    "id": "textId"
                                }
                            },
                            "format": "n/a",
                            "id": "textInfo"
                        }
                    ],
                    "format": "n/a",
                    "id": "20220831"
                }
            ],
            "format": "n/a",
            "id": "textRecord"
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
