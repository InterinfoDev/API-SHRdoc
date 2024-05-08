# appForgotPwd 
執行忘記密碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appForgotPwd
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {uid:admin} | Object | 將帳號組成物件 |


### JSON representation
Here is a JSON representation of request.
```json
{
  "request":{
      "uid":"admin"
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
| uid  | admin | String | 登入帳號 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "resetPwd":{
         "id":"resetPwd",
         "name":"忘記密碼執行結果",
         "value":{
            "validationEmail":{ --lucas
               "id":"validationEmail", --lucas
               "name":"電子郵件",
               "value":"xxx@interinfo.com.tw",
               "type":"string",
               "format":"email"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "email":"電子郵件",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
