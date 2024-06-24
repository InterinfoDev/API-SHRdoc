# appChangePwdRule
密碼過期更新密碼規則

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appChangePwd
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {} | Object | 請將帳號密碼組成物件 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "request":{
  }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| request | Object | 要求本文 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "查詢成功"
   ],
   "data":{
      "checkRule":{
         "name":"清單資訊",
         "type":"array",
         "value":{
            "checkUppercase":{
               "name":"大寫長度需大於等於",
               "type":"integer",
               "value":1,
               "format":"n/a",
               "id":"checkUppercase"
            },
            "checkNumLength":{
               "name":"數字長度需大於等於",
               "type":"integer",
               "value":1,
               "format":"n/a",
               "id":"checkNumLength"
            },
            "checkLowercase":{
               "name":"小寫長度需大於等於",
               "type":"integer",
               "value":1,
               "format":"n/a",
               "id":"checkLowercase"
            },
            "checkLength":{
               "name":"總長度需大於等於",
               "type":"integer",
               "value":8,
               "format":"n/a",
               "id":"checkLength"
            }
         },
         "format":"n/a",
         "id":"detail"
      },
      "checkState":{
         "name":"查詢狀態",
         "type":"object",
         "value":{
            "resultType":{
               "name":"回傳結果",
               "type":"string",
               "value":"success",
               "format":"n/a",
               "id":"resultType"
            }
         },
         "format":"n/a",
         "id":"checkState"
      }
   }
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
