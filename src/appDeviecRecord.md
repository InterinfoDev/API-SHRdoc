# appDeviceRecord
紀錄裝置識別碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appDeviceRecord
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
| request | {token:085A1C92-5A50-47AD-8853-CE3330F28D74,deviceId:TEST_DEVICE_ID,deviceName:xxx的iphone,deviceType:ios,series:iPhone13,version:15.4} | Object | 異動條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "token":"085A1C92-5A50-47AD-8853-CE3330F28D74",
      "deviceId":"TEST_DEVICE_ID",
      "deviceName":"XXX的iphone",
      "deviceType":"ios",
      "series":"iPhone13",
      "version":"15.4"
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
| token | 085A1C92-5A50-47AD-8853-CE3330F28D74 | 識別碼| 修改欄位 | Y | n/a | |
| deviceId | TEST_DEVICE_ID | 裝置識別碼 | 欄位代號 | Y | n/a |  |
| deviceName | xxx的iphone | String | 裝置名稱 | N | n/a |  |
| deviceType | iOS | String | 裝置類別 | N | n/a |  |
| series | iPhone13 | String | 裝置系列 | N | n/a |  |
| version | 15.4 | String | 裝置版本號 | N | n/a |  |

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
      "deviceRecord":{
         "name":"識別碼裝置異動",
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
         "id":"deviceRecord"
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
