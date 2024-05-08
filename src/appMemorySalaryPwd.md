# appMemorySalaryPwd 
生物辨識記憶密碼驗證員工薪資條密碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appMemorySalaryPwd
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
| request | {salaryPwd:98628727872926023198} | Object | 查詢條件


### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820", 
    "request":{ 
        'salaryPwd':'98628727872926023198'
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
| salaryPwd  | 98628727872926023198 | String | 薪資條密碼 | Y | n/a |

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
