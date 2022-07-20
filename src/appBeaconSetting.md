# appBeaconSetting
取得可打卡的Beacon

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBeaconSetting
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
| request | {} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
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
      "beacon":{
         "name":"beacon",
         "type":"array",
         "value":[
            {
               "name":"beacon資訊",
               "type":"object",
               "value":{
                  "beaconMajor":{
                     "name":"主要",
                     "type":"string",
                     "value":"1",
                     "format":"n/a",
                     "id":"beaconMajor"
                  },
                  "beaconName":{
                     "name":"beacon名稱",
                     "type":"string",
                     "value":"beacon test",
                     "format":"n/a",
                     "id":"beaconName"
                  },
                  "beaconMinor":{
                     "name":"次要",
                     "type":"string",
                     "value":"21356",
                     "format":"n/a",
                     "id":"beaconMinor"
                  },
                  "beaconUuid":{
                     "name":"beacon代碼",
                     "type":"string",
                     "value":"B5B182C7-EAB1-4988-AA99-B5C1517008D7",
                     "format":"n/a",
                     "id":"beaconUuid"
                  }
               },
               "format":"n/a",
               "id":"beaconInfo"
            },
            {
               "name":"beacon資訊",
               "type":"object",
               "value":{
                  "beaconMajor":{
                     "name":"主要",
                     "type":"string",
                     "value":"1",
                     "format":"n/a",
                     "id":"beaconMajor"
                  },
                  "beaconName":{
                     "name":"beacon名稱",
                     "type":"string",
                     "value":"beacon 測試",
                     "format":"n/a",
                     "id":"beaconName"
                  },
                  "beaconMinor":{
                     "name":"次要",
                     "type":"string",
                     "value":"21356",
                     "format":"n/a",
                     "id":"beaconMinor"
                  },
                  "beaconUuid":{
                     "name":"beacon代碼",
                     "type":"string",
                     "value":"A1A182C7-EAB1-4988-AA99-B5C1517006E1",
                     "format":"n/a",
                     "id":"beaconUuid"
                  }
               },
               "format":"n/a",
               "id":"beaconInfo"
            }
         ],
         "format":"n/a",
         "id":"beacon"
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
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "status":"success",
   "message":[
      "查無資料"
   ],
   "data":{
      "beacon":{
         "name":"beacon",
         "type":"array",
         "value":[
            
         ],
         "format":"n/a",
         "id":"beacon"
      },
      "properties":{
         "format":{
            "n/a":""
         }
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
