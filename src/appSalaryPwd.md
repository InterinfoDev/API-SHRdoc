# appSalaryPwd 
驗證員工薪資條密碼(獎金通用)

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSalaryPwd
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
| request | {salaryPwd:1234} | Object | 查詢條件


### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 取消empid傳入，改用getUser
        "salaryPwd":"1234"
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
| salaryPwd  | 1234 | String | 薪資條密碼 | Y | n/a |

### HTTP Response when Passowrd correct
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "checkPwd":{
         "id":"checkPwd",
         "name":"驗證薪資條密碼(獎金通用)",
         "value":true,
         "type":"boolean",
         "format":"n/a"
      },
      "key":{
         "id":"key",
         "name":"通行金鑰",
         "value":"32262008498747441193712198021232260366087649257856381618231",
         "type":"string",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when Passowrd incorrect
無論驗證與否，只會拋出錯誤的情況
```json 
{  -- lucas 增加案例
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "checkPwd":{
         "id":"checkPwd",
         "name":"驗證薪資條密碼(獎金通用)",
         "value":false,
         "type":"boolean",
         "format":"n/a"
      },
      "key":{
         "id":"key",
         "name":"通行金鑰",
         "value":"",
         "type":"string",
         "format":"n/a"
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
