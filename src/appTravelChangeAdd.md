# appTravelChangeAdd
員工出差變更

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelChangeAdd
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
| request | {'oldPno':'K00202206290001','pno':'K00202206290001','startDate':'20220629','endDate':'20220630','startTime':'1230','endTime':'1830','note':'測試出差變更備註','amt':16,'travelPlace':'台北南港','isHoliday':false,'isBusinessTrip':false,'version':2}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
     "oldPno":"K00202206290001",
     "pno":"K00202206290001",
     "startDate":"20220629",
     "endDate":"20220630",
     "startTime":"1230",
     "endTime":"1830",
     "note":"測試出差變更備註",
     "amt":16,
     "travelPlace":"台北南港",
     "isHoliday":false,
     "isBusinessTrip":false,
     "version":2
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
| oldPno | xxx | String | 原始出差單號 | Y | n/a |
| pno | xxx | String | 變更單號 | Y | n/a |
| startDate | 20220628 | String | 起始日期 | Y | YYYYmmdd |
| endDate | 20220630 | String | 結束日期 | Y | YYYYmmdd |
| startTime | 1900 | String | 起始時間 | Y | HHmm |  
| endTime | 2300 | String | 結束時間 | Y | HHmm |         
| note | test | String | 變更事由 | N | n/a |
| travelPlace | 台北南港 | String | 出差地點 | Y | n/a |
| version | 2 | Integer | 版次 | Y | n/a |
| amt | 300.0 | Decimal | 出差總計 | Y | n/a |
| isHoliday | false | boolean | 是否包含假日 | Y | n/a |
| isBusinessTrip | false | boolean | 具公差性質 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "addTravelChange":{
         "name":"新增出差變更單",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"存檔完成",
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
         "id":"addTravelChange"
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
