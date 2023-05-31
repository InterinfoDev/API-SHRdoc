# appChatSendText
發送訊息

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSappChatSendTextendText
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
| request | {'roomId':'xxx' ,'textId':'xxx', 'text':'' ,'textType':'img' ,'file':{'fileName':'kevin測試照片.jpg','fileData':'base64'}, 'reply':{'sender':'xxx','textId':'xxx','content':'xxx','textType':'xxx','timestamp':''}} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "roomId":"315f7d13-7d1f-401e-a208-b5cba320b8f1", 
      "textId":"315f7d13-7d1f-401e-a208-b5cba320b8f1", 
      "text":"",
      "textType":"img",
      "file":{
        "fileName":"kevin.jpg",
        "fileData":"base64"
      },
       "reply":{
        "sender":"xxx",
        "textId":"xxx",
        "textType":"xxx",
        "content":"xxx",
        "timestamp":"xxx"
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
| roomId | 123456789 | String | 聊天室鍵值 | Y | n/a |
| textId | 123456789 | String | 訊息鍵值 | Y | n/a |
| text |  | String | 訊息內容(如果類型為圖片或是檔案放空白即可) | N | n/a |
| textType | img | String | 訊息類型 | Y | n/a |
| file |  | String | 附件檔案 |  | n/a |
| fileName | test.jpg | String | 附件檔案 | N | n/a |
| fileData | String | 附件檔案 | N | base64 |
| reply | Object | 回覆內容 |  | n/a |
| timestamp | String | 時間戳 | N | n/a |

### TextType
| textType | Description |
|:---------|:------------|
| text | 一般訊息 |
| sysText | 系統訊息 |
| img | 圖片 |
| file | 檔案 |
| replyFile | 回覆檔案 |
| replyImg | 回覆圖片 |
| replyText | 回覆文字 |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "properties": {}
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
