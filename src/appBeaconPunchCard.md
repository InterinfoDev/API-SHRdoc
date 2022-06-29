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
| request | {"beaconId":"B5B182C7-EAB1-4988-AA99"} | Object | 打卡資訊

### JSON representation
Here is a JSON representation of request.
```json
{ 
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "beaconId":
          {
            "B5B182C7-EAB1-4988-AA99"
          },
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
               "value":"20220628",
               "format":"YYYYmmdd",
               "id":"punchDate"
            },
            "punchTime":{
               "name":"實際打卡時間",
               "type":"string",
               "value":"1758",
               "format":"HHmm",
               "id":"punchTime"
            },
            "punchResult":{
               "name":"實際打卡結果",
               "type":"object",
               "value":{
                  "errorMessage":{
                     "name":"錯誤訊息",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"errorMessage"
                  },
                  "isError":{
                     "name":"是否為錯誤打卡",
                     "type":"boolean",
                     "value":false,
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
                  "errorMessage":{
                     "name":"錯誤訊息",
                     "type":"string",
                     "value":"資料異動失敗",
                     "format":"n/a",
                     "id":"errorMessage"
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
