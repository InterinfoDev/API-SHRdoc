# appMemoryPwd 
生物辨識記憶密碼驗證員工登入密碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appMemoryPwd
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {uid:admin,pwd:admin} | Object | 查詢條件


### JSON representation
Here is a JSON representation of request.
```json
{
   "request":{
      "uid":"admin",
      "pwd":"admin"
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
| pwd  | admin | String | 登入密碼 | Y | n/a |
| uid  | admin | String | 使用者 | Y | n/a |
### HTTP Response when Passowrd correct
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "result":{
         "name":"核對結果",
         "type":"boolean",
         "value":true,
         "format":"n/a",
         "id":"result"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      }
   }
}


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
