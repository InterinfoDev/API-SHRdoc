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
