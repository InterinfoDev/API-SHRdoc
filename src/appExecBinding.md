# appExecBinding
綁定裝置

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appExecBinding
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
| request | {deviceBindId:test,deviceType:ios} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "deviceBindId":"test",
   "deviceType":"ios"
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
            "bindingDate":{
               "name":"綁定日期",
               "type":"string",
               "value":"20240123",
               "format":"n/a",
               "id":"bindingDate"
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
               "type":"integer",
               "value":"ios",
               "format":"n/a",
               "id":"bindingTpe"
            },
            "bindingTime":{
               "name":"綁定時間",
               "type":"string",
               "value":"160329",
               "format":"n/a",
               "id":"bindingTime"
            },
            "id":{
               "name":"綁定ID",
               "type":"string",
               "value":"0:0:0:0:0:0:0:1",
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
