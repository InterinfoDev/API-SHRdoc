# appLogin
驗證使用者帳號密碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appLogin
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {uid:admin,pwd:1234} | Object | 請將帳號密碼組成物件 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "request":{
      "uid":"admin",
      "pwd":"1234"
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
| pwd | 1234 | String | 登入密碼 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "uid":"99660492215776850458",
      "right":"xxxxx",
      "empolyee":{
         "id":"empolyee",
         "name":"個人資訊",
         "value":{
            "empid":{
               "id":"empid",
               "name":"員工編號",
               "value":"L100387",
               "type":"string",
               "format":"n/a"
            },
            "fullName":{
               "id":"fullName",
               "name":"員工姓名",
               "value":"林奇杰",
               "type":"string",
               "format":"n/a"
            },
            "fulllEname":{
               "id":"fulllEname",
               "name":"員工英文姓名",
               "value":"Lucas",
               "type":"string",
               "format":"n/a"
            },
            "companyId":{
               "id":"companyId",
               "name":"公司代號",
               "value":"97090920",
               "type":"string",
               "format":"n/a"
            },
            "companySimpleName": {
               "name": "公司簡稱",
               "type": "string",
               "value": "72英特內(中和)",
               "format": "n/a",
               "id": "companySimpleName"
            },              
            "depNumber":{
               "id":"depNumber",
               "name":"部門暗碼",
               "value":1,
               "type":"integer",
               "format":"n/a"
            }
            "depSimpleName": {
               "name": "部門簡稱",
               "type": "string",
               "value": "研發處",
               "format": "n/a",
               "id": "depSimpleName"
            }
         },
         "type":"object",
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

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料，除非驗證失敗
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
