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
| request | {punchDate:20211126 , punchTime:1706 , gps:{lat:21.23444,lon:345.32344} , ip :117.24.10.125 , empid: admin} | Object | 打卡資訊


### JSON representation

Here is a JSON representation of request.

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "punchDate":"20211126",
        "punchTime":"1706",
        "gps":
          {
            "lat":21.23444,
            "lon":345.32344
          },
        "ip":"117.24.10.125",
        "empid":"admin"
    }
}
```


### Properties

| Property | Type | Description |
|:---------|:-----|:------------|
| **uid**   | String | 加密後帳號 |
| **right** | String | 加密後系統相關資料 |
| **request** | 要求本文 |

### request Properties

| Key | Value | Type | Description
|:----------|:-------------|:-----|:------------|
| punchDate | 20211126 | String | 打卡日期 |
| punchTime | 1706 | String | 打卡時間 |
| gps |  | Object | GPS定位點資訊 |
| lat | 21.23444 | Deciaml | 緯度 |
| lon | 345.32344 | Deciaml | 經度 |
| ip | 117.24.10.125 | String | 使用者裝置IP |
| empid | admin| String | 員工編號 |


### HTTP Response when Successful
```json
{
	{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "gpsPunchCard":{
         "id":"gpsPunchCard",
         "name":"GPS線上打卡結果",
         "value":{
            "punchInfo":{
               "id":"punchInfo",
               "name":"打卡資料",
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
                        "isWarrning":{
                           "id":"isWarrning",
                           "name":"是否發生警示打卡",
                           "value":true,
                           "type":"boolean",
                           "format":"n/a"
                        },
                        "warrningMessage":{
                           "id":"warrningMessage",
                           "name":"警示訊息",
                           "value":"XXXXXXX",
                           "type":"string",
                           "format":"n/a"
                        },
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
    "code": 406,
    "message": [
        "系統錯誤"
    ],
    "data": {}
}
```
