# appRecognitionTerms
查詢使用者公司法規條文

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appRecognitionTerms
```

### HTTP Request Mehod
```
POST
```


### Request body
| Property | Type | Description |
|:---------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {locale : US} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "locale":"US"
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
| locale | US | String | 語系 | N | n/a |

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
      "recognitionTerms":{
         "name":"法條資訊",
         "type":"object",
         "value":{
            "termsContent":{
               "name":"法條內文",
               "type":"string",
               "value":"公司別TW 測試條款",
               "format":"n/a",
               "id":"termsContent"
            }
         },
         "format":"n/a",
         "id":"recognitionTerms"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，沒有設定公司別或通用資料
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "查無設定檔"
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
