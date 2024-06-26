# appCompanySuper
取得某員工公司別可視範圍資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appCompanySuper
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {} | Object | 查詢條件 |


### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 移除empid 條件，改用getUser
    }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "companySuper":{  --lucas 改名companySuper
         "id":"companySuper",
         "name":"公司查詢權限",
         "value":[
            {
               "id":"company",  --lucas  改名company
               "name":"公司資訊",
               "value":{
                  "companyId":{
                     "id":"companyId",
                     "name":"公司代號",
                     "value":"97090920",
                     "type":"string",
                     "format":"n/a"
                  },
                  "companyFullName":{
                     "id":"companyFullName",
                     "name":"公司全名",
                     "value":"英特內軟體股份有限公司",
                     "type":"string",
                     "format":"n/a"
                  },
                  "companySimpleName":{
                     "id":"companySimpleName",
                     "name":"公司簡稱",
                     "value":"英特內軟體",
                     "type":"string",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
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
