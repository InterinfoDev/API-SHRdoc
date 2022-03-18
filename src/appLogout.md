# appLogout
記錄使用者登出資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appLogout
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
      "登出成功"
   ],
   "data":{
      "logout":{
         "logoutTime":{
            "name":"登出時間",
            "type":"string",
            "value":"1404",
            "format":"HHmm",
            "id":"logoutTime"
         },
         "logoutDate":{
            "name":"登出日期",
            "type":"string",
            "value":"20220318",
            "format":"YYYYmmdd",
            "id":"logoutDate"
         }
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

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料，除非驗證失敗
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "登出失敗"
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
