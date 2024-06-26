# appChatGroupSend
群傳

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChatGroupSend
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
| request | {'employeeId':['admin'] ,'text':'' ,'textType':'img' ,'file':{'fileName':'kevin測試照片.jpg','fileData':'base64'}} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{ 
      "employeeId":["admin"], 
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
| employeeId | [admin] | Array(String) | 群傳成員 | Y | n/a |
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
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "sendText":{
         "name":"發送訊息",
         "type":"object",
         "value":{
            "sendTime":{
               "name":"發送時間",
               "type":"string",
               "value":"1435",
               "format":"HHmm",
               "id":"sendTime"
            },
            "sendDate":{
               "name":"發送日期",
               "type":"string",
               "value":"20220914",
               "format":"YYYYmmdd",
               "id":"sendDate"
            },
         },
         "format":"n/a",
         "id":"sendText"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":""
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
