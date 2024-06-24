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
| request | {uid:admin,pwd:1234,deviceBindId:test,deviceType:ios,fieldKey:uid} | Object | 請將帳號密碼組成物件 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "request":{
      "uid":"admin",
      "pwd":"1234",
      "newPwd":"test",
      "checkNewPwd":"test",
      "fieldKey":"uid"
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
| uid | admin | String | 登入帳號 | Y | n/a |
| pwd | 1234 | String | 登入舊密碼 | Y | n/a |
| newPwd | 12345 | String | 登入新密碼 | Y | n/a |
| checkNewPwd | 12345 | String | 登入新密碼確認 | Y | n/a |
| fieldKey | uid | String | 檢核欄位的key | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "符合修改資料格式"
   ],
   "data":{
      "checkState":{
         "name":"更新狀態",
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

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料，除非驗證失敗
```json
{
   "status":"fail",
   "code":500,
   "message":[
      "請輸入更安全的密碼，密碼強度為：至少8碼，包含1碼以上大寫英文、1碼以上小寫英文、1碼以上數字!Please enter a more secure password, the password strength is: at least 8 words , including 1 or more uppercase English 1 or more lowercase English、1 or more digits!"
   ],
   "data":{
      "checkState":{
         "name":"更新狀態",
         "type":"object",
         "value":{
            "resultType":{
               "name":"回傳結果",
               "type":"string",
               "value":"error",
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
