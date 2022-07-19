# appExecIrregularOvertime
異動加班異常

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appExecIrregularOvertime
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {code:A01,errorData:[{companyId:TW,empid:admin,irragularDate:20220615}]} | Object | 異動條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "code":"A01",
        "errorData":[
         {
            "companyId":"TW",
            "empid":"admin",
            "irragularDate":"20220615"
         }
      ]
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| code | A01 | String | 異常回應 | true | n/a |  |
| errorData |  | Vector | 放key值 | n/a | n/a |  |
| companyId | TW | String | 公司別 | n/a | n/a |  |
| empid | admin | String | 員工編號 | n/a | n/a |  |
| irragularDate | 20220615 | String | 日期 | YYYYmmdd | n/a |  |



### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "notification":{
         "name":"更新通知",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"異動成功",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
            }
         },
         "format":"n/a",
         "id":"notification"
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
