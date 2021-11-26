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
| request | {"uid:"admin","pwd":"1234"} | Object | 請將帳號密碼組成物件 |


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
| **uid**   | String | 帳號 |
| **pwd** | String | 密碼 |


### HTTP Response Code 200
```json
{
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
