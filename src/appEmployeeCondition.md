# appEmployeeCondition
取得某員工可視範圍員工資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appEmployeeCondition
```

### HTTP Request Mehod
```
POST
```

### Request body
| Property | Type | Description |
|:---------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {companyId:97090920 , depNumber:[1] } | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{  --lucas 取消empid傳入，若有需要者改用getUser判斷
        "companyId":"97090920",
        "depNumber":[1],  --lucas 改成array 改名  並改成integer傳入
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
| companyId | 97090920 | String | 公司代號 | N | n/a |
| depNumber | [1] | Array(Integer) | 部門代號 | N | n/a |

### Use Function
| FunctionName | Request |
|:---------|:-----|
| 簽核代理人 | {'companyId':'' , 'depNumber':[]} |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "employeeCondition":{  --lucas 改名employeeCondition
         "id":"employeeCondition",
         "name":"人員查詢權限",
         "value":[
            {
               "id":"employee", --lucas 改名
               "name":"員工資訊",
               "value":{
                  "empFullName":{  --lucas 改名
                     "id":"empFullName", --lucas 改名
                     "name":"員工中文姓名",
                     "value":"林奇杰",
                     "type":"string",
                     "format":"n/a"
                  },
                  "empFullEname":{--lucas 改名
                     "id":"empFullEname",--lucas 改名
                     "name":"員工英文姓名",
                     "value":"Lucas",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depNumber":{
                     "id":"depNumber",
                     "name":"部門暗碼",
                     "value":2,
                     "type":"integer",
                     "format":"n/a"
                  },
                  "depCode":{
                     "id":"deoCode",
                     "name":"部門代號",
                     "value":"D2000",
                     "type":"string",
                     "format":"n/a"
                  },
                  "depName":{
                     "id":"depName",
                     "name":"部門名稱",
                     "value":"CTO",
                     "type":"string",
                     "format":"n/a"
                  },
                  "empid":{
                     "id":"empid",
                     "name":"員工編號",
                     "value":"L100387",
                     "type":"string",
                     "format":"n/a"
                  },
                  "position":{
                     "id":"position",
                     "name":"職稱",
                     "value":"CTO",
                     "type":"string",
                     "format":"n/a"
                  },
                  "photo":{
                     "id":"photo",
                     "name":"員工照片",
                     "value":"base64url",
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
