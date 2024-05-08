# appTemperatureInterface
查詢體溫裝置介面

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTemperatureInterface
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
| request | {} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{}
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
      "temperatureInterface":{
         "id":"temperatureInterface",
         "name":"裝置資訊",
         "value":[
            {
               "id":"device",  --Andy 裝置資訊的value多一層,將deviceId和deviceName移動至device的value
               "name":"介面資訊",
               "value":{
                  "deviceId":{
                     "id":"deviceId",
                     "name":"介面代號",
                     "value":"A",
                     "type":"string",
                     "format":"n/a"
                  },
                  "deviceName":{
                     "id":"deviceName",
                     "name":"介面名稱",
                     "value":"額溫槍",
                     "type":"string",
                     "format":"n/a"
                  }
               },
               "type":"string",
               "format":"n/a"
            },
            {
               "id":"device",
               "name":"介面資訊",
               "value":{
                  "deviceId":{
                     "id":"deviceId",
                     "name":"介面代號",
                     "value":"B",
                     "type":"string",
                     "format":"n/a"
                  },
                  "deviceName":{
                     "id":"deviceName",
                     "name":"介面名稱",
                     "value":"耳溫槍",
                     "type":"string",
                     "format":"n/a"
                  }
               },
               "type":"string",
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
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "XXX"
    ],
    "data":{
      "temperatureInterface":{
         "id":"temperatureInterface",
         "name":"裝置資訊",
         "value":[],
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
