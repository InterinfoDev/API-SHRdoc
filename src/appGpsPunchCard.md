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
| request | {punchDate:20211126 , punchTime:1706 , gps:{latitude:21.23444,longitude:345.32344} , ip :117.24.10.125 } | Object | 打卡資訊

### JSON representation
Here is a JSON representation of request.
```json
{ --lucas 取消empid，改用getUser
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "punchDate":"20211126",
        "punchTime":"1706",
        "gps":
          {
            "latitude":21.23444, --lucas改名
            "longitude":345.32344 --lucas改名
          },
        "ip":"117.24.10.125"
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
| punchDate | 20211130 | String | 打卡日期 | Y | AC(YYYYmmdd) |
| punchTime | 1801 | String | 打卡時間 | Y | TIME(HHmm) |
| gps |  | Object | GPS資訊 | Y | n/a |
| latitude | 21.23444 | Decimal | 緯度 | Y | GPS Location Data |
| longitude | 345.32344 | Decimal | 經度 | Y | GPS Location Data |
| ip | 117.24.10.125 | String | IP位置 | Y | IP Address(xx.xx.xx.xx) |

### HTTP Response when Successful
```json
{ 
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "gpsPunchCard":{ --lucas 移除punch 這層 20211210
         "id":"gpsPunchCard",
         "name":"GPS線上打卡結果",
         "value":{ 
              "punchDate":{
                 "id":"punchDate",
                 "name":"實際打卡日期",
                 "value":"20211122",
                 "type":"string",
                 "format":"YYYYmmdd"
              },
              "punchTime":{
                 "id":"punchTime",
                 "name":"實際打卡時間",
                 "value":"0911",
                 "type":"string",
                 "format":"HHmm"
              },
              "punchResult":{
                 "id":"punchResult",
                 "name":"實際打卡結果",
                 "value":{
                    "isError":{
                       "id":"isError",
                       "name":"是否為錯誤打卡",
                       "value":true,
                       "type":"boolean",
                       "format":"n/a"
                    },
                    "errorMessage":{
                       "id":"errorMessage",
                       "name":"錯誤訊息(如果isError為true，代表使用者要重新打卡)",
                       "value":"XXXXXXX",
                       "type":"string",
                       "format":"n/a"
                    }
                 },
                 "type":"object",
                 "format":"n/a"
              }
            },
         
         "type":"object",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":"",
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分"
         }
      }
   }
}
```

### HTTP Response when Punch Failed
打卡失敗的時候，需考慮 punchResult 內的isError=true
```json
{ --lucas增加案例
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "gpsPunchCard":{
         "id":"gpsPunchCard",
         "name":"GPS線上打卡結果",
         "value":{ --lucas 移除punch 這層 20211210
              "punchDate":{
                 "id":"punchDate",
                 "name":"實際打卡日期",
                 "value":"20211122",
                 "type":"string",
                 "format":"YYYYmmdd"
              },
              "punchTime":{
                 "id":"punchTime",
                 "name":"實際打卡時間",
                 "value":"0911",
                 "type":"string",
                 "format":"HHmm"
              },
              "punchResult":{
                 "id":"punchResult",
                 "name":"實際打卡結果",
                 "value":{
                    "isError":{
                       "id":"isError",
                       "name":"是否為錯誤打卡",
                       "value":true,
                       "type":"boolean",
                       "format":"n/a"
                    },
                    "errorMessage":{
                       "id":"errorMessage",
                       "name":"錯誤訊息(如果isError為true，代表使用者要重新打卡)",
                       "value":"XXXXXXX",
                       "type":"string",
                       "format":"n/a"
                    }
                 },
                 "type":"object",
                 "format":"n/a"
              }
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":"",
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分"
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
