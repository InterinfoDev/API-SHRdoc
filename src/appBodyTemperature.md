# appBodyTemperature
回報當日體溫

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBodyTemperature
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
| request | {measureDate :20211202,measureTime :0830, empid:admin, bodyTemperature:36.5, measureInterface:A, measureUnit:C} | Object | 送出資料

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 移除empid，改用getUser
        "measureDate":"20211202", 
        "measureTime":"0830", 
        "bodyTemperature":36.5, 
        "measureInterface":"A", 
        "measureUnit":"C", 
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
| measureDate | 20211202 | String | 測量日期 | Y | AC(YYYYmmdd) |
| measureTime | 0830 | String | 測量時間 | Y | TIME(HHmm) |
| bodyTemperature | 36.5 | Decimal | 測量溫度 | Y | Degrees |
| measureInterface | A | String | 測量介面 | Y | A額溫槍,B耳溫搶,C體溫計,D紅外線熱像儀 |
| measureUnit | C | String | 測量單位 | Y | F 華氏 C 攝氏 |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "bodyTemperature":{
         "id":"bodyTemperature",
         "name":"體溫資訊",
         "value":{
            "executeResult":{
               "id":"executeResult",  --lucas 增加
               "name":"異動結果",
               "value":true,
               "type":"boolean",
               "format":"n/a"
            },
            "temperatureInfo":{
               "id":"temperatureInfo",
               "name":"體溫資料",
               "value":{
                  "temperature":{
                     "id":"temperature",
                     "name":"測量體溫",
                     "value":38.5,
                     "type":"decimal",
                     "format":"degrees"
                  },
                  "temperatureUnit":{
                     "id":"temperatureUnit",
                     "name":"測量單位",
                     "value":"celsius/fahrenheit",
                     "type":"string",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            "interface":{
               "id":"interface",
               "name":"測量介面",
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
               "type":"object",
               "format":"n/a"
            },
            "warrning":{
               "id":"warrning",
               "name":"警示提醒",
               "value":{
                  "isWarrning":{
                     "id":"isWarrning",
                     "name":"是否為警示範圍",
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
            "degrees":"度數"
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
