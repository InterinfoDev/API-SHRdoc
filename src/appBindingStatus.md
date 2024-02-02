# appBindingStatus
查詢綁定狀態

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBindingStatus
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
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "bindingInformation":{
         "name":"綁定狀態資訊",
         "type":"object",
         "value":{
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
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "levelDescription":{
               "name":"機制說明",
               "type":"string",
               "value":"詢問綁定\r\n當貴司採用詢問綁定機制，登入時，系統自動詢問使用者是否綁定裝置，可選擇性決定是否綁定裝置，以降低資訊外洩的風險。\r\n",
               "format":"n/a",
               "id":"levelDescription"
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
               "value":"121751",
               "format":"n/a",
               "id":"bindingTime"
            },
            "id":{
               "name":"綁定編號",
               "type":"string",
               "value":"test",
               "format":"n/a",
               "id":"id"
            },
            "level":{
               "name":"綁定機制",
               "type":"integer",
               "value":2,
               "format":"n/a",
               "id":"level"
            }
         },
         "format":"n/a",
         "id":"bindingInformation"
      }
   }
}
```

### HTTP Response when No Data
無資料則顯示設定檔資料或是預設資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "bindingInformation":{
         "name":"綁定狀態資訊",
         "type":"object",
         "value":{
            "levelDescription":{
               "name":"機制說明",
               "type":"string",
               "value":"詢問綁定\r\n當貴司採用詢問綁定機制，登入時，系統自動詢問使用者是否綁定裝置，可選擇性決定是否綁定裝置，以降低資訊外洩的風險。\r\n",
               "format":"n/a",
               "id":"levelDescription"
            },
            "level":{
               "name":"綁定機制",
               "type":"integer",
               "value":2,
               "format":"n/a",
               "id":"level"
            }
         },
         "format":"n/a",
         "id":"bindingInformation"
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
