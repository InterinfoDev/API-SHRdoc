# appGpsPunchCard
GPS線上打卡

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appGpsPunchCard
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
| request | {gps:{latitude:21.23444,longitude:345.32344}, pushType:B} | Object | 打卡資訊

### JSON representation
Here is a JSON representation of request.
```json
{ --lucas 取消empid，改用getUser
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "gps":
          {
            "latitude":21.23444, --lucas改名
            "longitude":345.32344 --lucas改名
          }
         "pushType":"B"
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
| gps |  | Object | GPS資訊 | Y | n/a |
| latitude | 21.23444 | Decimal | 緯度 | Y | GPS Location Data |
| longitude | 345.32344 | Decimal | 經度 | Y | GPS Location Data |
| pushType | B | String | 打卡方式 | Y | n/a |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "gpsPunchCard": {
            "name": "GPS線上打卡結果",
            "type": "object",
            "value": {
                "errorMessage": {
                    "name": "錯誤訊息",
                    "type": "string",
                    "value": "",
                    "format": "n/a",
                    "id": "errorMessage"
                },
                "isError": {
                    "name": "是否為錯誤打卡",
                    "type": "boolean",
                    "value": false,
                    "format": "n/a",
                    "id": "isError"
                },
                "punchResult": {
                    "name": "實際打卡結果",
                    "type": "object",
                    "value": [
                        {
                            "name": "打卡項目",
                            "type": "string",
                            "value": "英特內GPS-12F",
                            "format": "n/a",
                            "id": "pushTypeName"
                        },
                        {
                            "name": "GPS-經度",
                            "type": "string",
                            "value": 24.9982389,
                            "format": "n/a",
                            "id": "latitude"
                        },
                        {
                            "name": "GPS-緯度",
                            "type": "string",
                            "value": 121.48677,
                            "format": "n/a",
                            "id": "longitude"
                        },
                        {
                            "name": "IP",
                            "type": "string",
                            "value": "0:0:0:0:0:0:0:1",
                            "format": "n/a",
                            "id": "ip"
                        },
                        {
                            "name": "實際打卡日期",
                            "type": "string",
                            "value": "20230322",
                            "format": "YYYYmmdd",
                            "id": "punchDate"
                        },
                        {
                            "name": "實際打卡時間",
                            "type": "string",
                            "value": "1538",
                            "format": "HHmm",
                            "id": "punchTime"
                        }
                    ],
                    "format": "n/a",
                    "id": "punchResult"
                }
            },
            "format": "n/a",
            "id": "gpsPunchCard"
        },
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        }
    }
}
```

### HTTP Response when Punch Failed
打卡失敗的時候，需考慮 punchResult 內的isError=true
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "gpsPunchCard":{
         "name":"GPS線上打卡結果",
         "type":"object",
         "value":{
            "errorMessage":{
               "name":"錯誤訊息",
               "type":"string",
               "value":"GPS位置 不符合",
               "format":"n/a",
               "id":"errorMessage"
            },
            "isError":{
               "name":"是否為錯誤打卡",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"isError"
            },
            "punchResult":{
               "name":"實際打卡結果",
               "type":"object",
               "value":[
                  {
                     "name":"打卡項目",
                     "type":"string",
                     "value":"英特內GPS-12F",
                     "format":"n/a",
                     "id":"pushTypeName"
                  },
                  {
                     "name":"GPS-經度",
                     "type":"string",
                     "value":21.23444,
                     "format":"n/a",
                     "id":"latitude"
                  },
                  {
                     "name":"GPS-緯度",
                     "type":"string",
                     "value":345.32344,
                     "format":"n/a",
                     "id":"longitude"
                  },
                  {
                     "name":"IP",
                     "type":"string",
                     "value":"0:0:0:0:0:0:0:1",
                     "format":"n/a",
                     "id":"ip"
                  },
                  {
                     "name":"實際打卡日期",
                     "type":"string",
                     "value":"20230322",
                     "format":"YYYYmmdd",
                     "id":"punchDate"
                  },
                  {
                     "name":"實際打卡時間",
                     "type":"string",
                     "value":"1529",
                     "format":"HHmm",
                     "id":"punchTime"
                  }
               ],
               "format":"n/a",
               "id":"punchResult"
            }
         },
         "format":"n/a",
         "id":"gpsPunchCard"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
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
