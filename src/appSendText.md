# appSendText
發送訊息

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSendText
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
| request | {'roomId':'315f7d13-7d1f-401e-a208-b5cba320b8f1' ,'text':'' ,'textType':'img' ,'file':{'fileName':'kevin測試照片.jpg','fileData':'base64'}} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "roomId":"315f7d13-7d1f-401e-a208-b5cba320b8f1", 
      "text":"",
      "textType":"img",
      "file":{
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
| roomId | 123456789 | String | 聊天室鍵值 | Y | n/a |
| text |  | String | 訊息內容(如果類型為圖片或是檔案放空白即可) | N | n/a |
| textType | img | String | 訊息類型 | Y | n/a |
| file |  | String | 附件檔案 |  | n/a |
| fileName | test.jpg | String | 附件檔案 | N | n/a |
| fileData |  | String | 附件檔案 | N | base64 |

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
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "sendText": {
      "name": "發送訊息",
      "type": "object",
      "value": {
        "sendTime": {
          "name": "發送時間",
          "type": "string",
          "value": "1354",
          "format": "HHmm",
          "id": "sendTime"
        },
        "timestamp": {                 -- richard 新增資料 timestamp
          "name": "時間戳",
          "type": "string",
          "value": "20220926135421220",
          "format": "n/a",
          "id": "timestamp"
        },
        "sendDate": {
          "name": "發送日期",
          "type": "string",
          "value": "20220926",
          "format": "YYYYmmdd",
          "id": "sendDate"
        },
        "sendMessage": {
          "name": "發送訊息",
          "type": "string",
          "value": "發送成功",
          "format": "n/a",
          "id": "sendMessage"
        },
        "isSend": {
          "name": "是否發送",
          "type": "boolean",
          "value": true,
          "format": "n/a",
          "id": "isSend"
        },
        "textId": {               -- richard 新增資料 textId
          "name": "訊息鍵值",
          "type": "string",
          "value": "4ffb1980-75bd-4ab0-b728-918829c63c46",
          "format": "n/a",
          "id": "textId"
        }
      },
      "format": "n/a",
      "id": "sendText"
    },
    "properties": {
      "format": {
        "HHmm": "時間時分",
        "YYYYmmdd": "西元年月日",
        "n/a": ""
      }
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
