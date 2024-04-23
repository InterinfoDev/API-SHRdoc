# appBeaconPunchCard
Beacon打卡

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBeaconPunchCard
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
| request | {"buttonKey":"xxxxxxx","beaconId":"B5B182C7-EAB1-4988-AA99", "major":1, "minor":1} | Object | 打卡資訊

### JSON representation
Here is a JSON representation of request.
```json
{ 
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "beaconId":"B5B182C7-EAB1-4988-AA99",
        "major":1,  --kevin 新增major
        "minor":1,    --kevin 新增minor
        "buttonKey":"xxxxxxx"
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
| beaconId | B5B182C7-EAB1-4988-AA99 | String | ID名稱 | Y | N/A |
| major | 1 | Integer | major | Y | N/A |
| minor | 1 | Integer | minor  | Y | N/A |
| buttonKey | xxxxxxx | String | 按鈕鍵值 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "beaconPunchCard":{
         "name":"Beacon打卡結果",
         "type":"object",
         "value":{
            "punchDate":{
               "name":"實際打卡日期",
               "type":"string",
               "value":"20240422",
               "format":"YYYYmmdd",
               "id":"punchDate"
            },
            "punchTime":{
               "name":"實際打卡時間",
               "type":"string",
               "value":"1922",
               "format":"HHmm",
               "id":"punchTime"
            },
            "punchResult":{
               "name":"實際打卡結果",
               "type":"object",
               "value":{
                  "isError":{
                     "name":"是否為錯誤打卡",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"isError"
                  },
                  "resultTitle":{
                     "name":"回傳標題",
                     "type":"string",
                     "value":"打卡成功",
                     "format":"n/a",
                     "id":"resultTitle"
                  },
                  "resultMessage":{
                     "name":"回傳訊息",
                     "type":"string",
                     "value":"時間:19:22\n務必前往系統再次確認",
                     "format":"n/a",
                     "id":"resultMessage"
                  }
               },
               "format":"n/a",
               "id":"punchResult"
            }
         },
         "format":"n/a",
         "id":"beaconPunchCard"
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

### HTTP Response when Punch Failed
打卡失敗的時候，需考慮 punchResult 內的isError=true
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "beaconPunchCard":{
         "name":"Beacon打卡結果",
         "type":"object",
         "value":{
            "punchDate":{
               "name":"實際打卡日期",
               "type":"string",
               "value":"20220628",
               "format":"YYYYmmdd",
               "id":"punchDate"
            },
            "punchTime":{
               "name":"實際打卡時間",
               "type":"string",
               "value":"1816",
               "format":"HHmm",
               "id":"punchTime"
            },
            "punchResult":{
               "name":"實際打卡結果",
               "type":"object",
               "value":{
                  "resultTitel":{
                     "name":"回傳標題",
                     "type":"string",
                     "value":"打卡成功",
                     "format":"n/a",
                     "id":"resultTitel"
                  },
                  "resultMessage":{
                     "name":"回傳訊息",
                     "type":"string",
                     "value":"時間:19:22\n務必前往系統再次確認",
                     "format":"n/a",
                     "id":"resultMessage"
                  },
                  "isError":{
                     "name":"是否為錯誤打卡",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"isError"
                  }
               },
               "format":"n/a",
               "id":"punchResult"
            }
         },
         "format":"n/a",
         "id":"beaconPunchCard"
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
