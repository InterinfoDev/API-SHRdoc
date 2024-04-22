# appPunchCardSetting
取得打卡按鈕資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPunchCardSetting
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {} | Object | n/a |

### JSON representation
Here is a JSON representation of request.
```json
{ 
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
    }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### HTTP Response when Successful

```

### HTTP Response when Successful2
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
      "button":{
         "name":"打卡按鈕資訊",
         "type":"array",
         "value":[
            {
               "name":"打卡按鈕資訊",
               "type":"object",
               "value":{
                  "buttonKey":{
                     "name":"按鈕鍵值",
                     "type":"string",
                     "value":"99924066065569631271",
                     "format":"n/a",
                     "id":"buttonKey"
                  },
                  "buttonName":{
                     "name":"按鈕名稱",
                     "type":"string",
                     "value":"打卡",
                     "format":"n/a",
                     "id":"buttonName"
                  }
               },
               "format":"n/a",
               "id":"buttonInfo"
            }
         ],
         "format":"n/a",
         "id":"button"
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
