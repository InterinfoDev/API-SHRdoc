# appTranslate
取得裝置端翻譯後訊息

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTranslate
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
| request | {'locale':'US','deviceType':'IOS'} | Object | 翻譯文字資訊

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "locale":"US",
      "deviceType":"IOS"
      ]
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
| locale | TW | String | 語系代號 | Y | n/a |
| deviceType | XXX | String | 裝置類型 | Y | IOS / Android |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "translateList":{
         "name":"翻譯資訊清單",
         "type":"object",
         "value":[
            {
               "name":"翻譯詳細資料",
               "type":"object",
               "value":{
                  "MessageId":{
                     "name":"訊息代號",
                     "type":"string",
                     "value":"employeeName",
                     "format":"n/a",
                     "id":"MessageId"
                  },
                  "Content":{
                     "name":"訊息內容",
                     "type":"string",
                     "value":"Name",
                     "format":"n/a",
                     "id":"Content"
                  }
               },
               "format":"n/a",
               "id":"translateDetail"
            },
            {
               "name":"翻譯詳細資料",
               "type":"object",
               "value":{
                  "MessageId":{
                     "name":"訊息代號",
                     "type":"string",
                     "value":"empId",
                     "format":"n/a",
                     "id":"MessageId"
                  },
                  "Content":{
                     "name":"訊息內容",
                     "type":"string",
                     "value":"ID",
                     "format":"n/a",
                     "id":"Content"
                  }
               },
               "format":"n/a",
               "id":"translateDetail"
            }
         ],
         "format":"n/a",
         "id":"translateList"
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
無翻譯資料傳入也會回傳成功，翻譯資訊清單回傳為空
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "translateList":{
         "name":"翻譯資訊清單",
         "type":"object",
         "value":[],
         "format":"n/a",
         "id":"translateList"
      },
      "properties":{
         "format":{
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
