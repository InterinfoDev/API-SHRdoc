# appExecBinding
綁定裝置

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appExecBinding
```

### HTTP Request Method
```
POST
```


### Request body
| Property | Type | Description |
|:---------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {deviceBindId:test,deviceType:ios} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "deviceBindId":"test",
   "deviceType":"ios",
   "hardwareModel":"iphone14"
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
| deviceBindId | test | String | 綁定id | N | n/a |
| deviceType | ios | String | 綁定類型 | N | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "executeMessage":{
         "name":"異動訊息",
         "type":"string",
         "value":"裝置綁定成功",
         "format":"n/a",
         "id":"executeMessage"
      },
      "executeResult":{
         "name":"異動結果",
         "type":"boolean",
         "value":true,
         "format":"n/a",
         "id":"executeResult"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "executeData":{
         "name":"異動後資料",
         "type":"object",
         "value":{
            "isBinding": {
                "name": "是否綁定",
                "type": "boolean",
                "value": true,
                "format": "n/a",
                "id": "isBinding"
            },
            "statusDescription": {
                "name": "綁定狀態說明",
                "type": "string",
                "value": "綁定中",
                "format": "n/a",
                "id": "statusDescription"
            },
            "hardwareModel":{
               "name":"硬體型號",
               "type":"string",
               "value":"iphone14",
               "format":"n/a",
               "id":"hardwareModel"
            },
            "bindingDate":{
               "name":"綁定日期",
               "type":"string",
               "value":"20240202",
               "format":"n/a",
               "id":"bindingDate"
            },
            "levelDescription":{
               "name":"機制說明",
               "type":"string",
               "value":"詢問綁定\r\n當貴司採用詢問綁定機制，登入時，系統自動詢問使用者是否綁定裝置，可選擇性決定是否綁定裝置，以降低資訊外洩的風險。\r\n",
               "format":"n/a",
               "id":"levelDescription"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "bindingType":{
               "name":"裝置類型",
               "type":"string",
               "value":"ios",
               "format":"n/a",
               "id":"bindingTpe"
            },
            "level":{
               "name":"綁定機制",
               "type":"integer",
               "value":2,
               "format":"n/a",
               "id":"level"
            },
            "bindingTime":{
               "name":"綁定時間",
               "type":"string",
               "value":"122020",
               "format":"n/a",
               "id":"bindingTime"
            },
            "id":{
               "name":"綁定編號",
               "type":"string",
               "value":"test",
               "format":"n/a",
               "id":"id"
            }
         },
         "format":"n/a",
         "id":"executeData"
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
