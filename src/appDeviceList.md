# appDeviceList
取得使用者裝置清單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appDeviceList
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

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| vacationYM | 202201 | String | 查詢年月 | Y | AC(YYYYmm) |
| empid | admin | String | 員工編號 | Y | n/a |

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
      "deviceList":{
         "name":"裝置清單",
         "type":"array",
         "value":[
            {
               "name":"裝置資訊",
               "type":"object",
               "value":{
                  "deviceName":{
                     "name":"裝置名稱",
                     "type":"string",
                     "value":"sdk_gphone_x86",
                     "format":"n/a",
                     "id":"deviceName"
                  },
                  "series":{
                     "name":"裝置系列",
                     "type":"string",
                     "value":"google sdk_gphone_x86",
                     "format":"n/a",
                     "id":"series"
                  },
                  "deviceType":{
                     "name":"裝置類別",
                     "type":"string",
                     "value":"android",
                     "format":"n/a",
                     "id":"deviceType"
                  },
                  "deviceId":{
                     "name":"裝置代號",
                     "type":"string",
                     "value":"a46de6485262585a",
                     "format":"n/a",
                     "id":"deviceId"
                  }
               },
               "format":"n/a",
               "id":"device"
            },
            {
               "name":"裝置資訊",
               "type":"object",
               "value":{
                  "deviceName":{
                     "name":"裝置名稱",
                     "type":"string",
                     "value":"xxx的iphone",
                     "format":"n/a",
                     "id":"deviceName"
                  },
                  "series":{
                     "name":"裝置系列",
                     "type":"string",
                     "value":"iPhone13",
                     "format":"n/a",
                     "id":"series"
                  },
                  "deviceType":{
                     "name":"裝置類別",
                     "type":"string",
                     "value":"ios",
                     "format":"n/a",
                     "id":"deviceType"
                  },
                  "deviceId":{
                     "name":"裝置代號",
                     "type":"string",
                     "value":"TEST_DEVICE_ID",
                     "format":"n/a",
                     "id":"deviceId"
                  },
                  "isNotifyDevice": {
                      "name": "是否為推播裝置",
                      "type": "boolean",
                      "value": true,
                      "format": "n/a",
                      "id": "isNotifyDevice"
                  }
               },
               "format":"n/a",
               "id":"device"
            }
         ],
         "format":"n/a",
         "id":"deviceList"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
