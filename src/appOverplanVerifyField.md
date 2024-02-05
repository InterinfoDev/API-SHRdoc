# appOverplanVerifyField
預定加班單畫面欄位檢核

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOverplanVerifyField
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
| request | {{'fieldName':'startTime', 'empid':'admin', 'startDate':'20220527', 'startTime':'1900', 'endTime':'2200', 'reason':'20220524kevinOverplanTest', 'payType':'A', 'totalPayHour':0.0, 'totalRestHour':0.0, 'specifyHour':0.0, 'oldEatHour':0.0, 'isEat':false, 'beforeWork':false}} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "fieldName":"startTime",
      "empid":"admin", 
      "startDate":"20220527",
      "startTime":"1900",    
      "endTime":"2200",      
      "reason":"20220524kevinOverplanTest",        
      "payType":"A",          
      "totalPayHour":0.0,
      "totalRestHour":0.0,
      "specifyHour":0.0,
      "oldEatHour":0.0,
      "isEat":false,
      "beforeWork":false
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
| fieldName | startTime | String | 欄位名稱 | Y | n/a |
| empid | admin | String | 員工編號 | N | n/a |
| startDate | 20220527 | String | 起始日期 | N | YYYYmmdd |
| startTime | 1900 | String | 起始時間 | N | HHmm |  
| endTime | 2300 | String | 結束時間 | N | HHmm |         
| reason | 20220524kevinOverplanTest | String | 請假說明 | N | n/a |
| payType | A | String | 給付方式 | N | n/a |
| totalPayHour | 0.0 | Decimal | 總計給薪時數 | N | hour | 
| totalRestHour | 0.0 | Decimal | 總計補休時數 | N | hour |
| specifyHour | 0.0 | Decimal | 指定用餐時間 | N | hour |
| oldEatHour | 0.0 | Decimal | 原用餐時間 | N | hour |
| isEat | false | boolean | 是否用餐 | N | n/a | 
| beforeWork | false | boolean | 跨日往前加班 | N | n/a | 

### Using Field
| FieldName | Description |
|:---------|:-----|
| startTime | 起始時間 |
| endTime | 結束時間 |
| payType | 給付方式 |
| isEat | 是否用餐 |
| specifyHour | 指定用餐時間 |
| totalPayHour | 總計給薪時數 |
| totalRestHour | 總計補休時數 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "verifyResult":{
         "name":"檢核結果",
         "type":"object",
         "value":{
            "actions":{
               "name":"異動欄位",
               "type":"object",
               "value":{
                  "setEditable":{
                     "name":"設定欄位可否編輯",
                     "type":"array",
                     "value":[
                        {  --kevin 補上資料
                           "name":"原用餐時間",
                           "type":"boolean",
                           "value":false,
                           "format":"N/A",
                           "id":"oldEatHour"
                        }
                     ],
                     "format":"n/a",
                     "id":"setEditable"
                  },
                  "setValue":{
                     "name":"設定欄位值",
                     "type":"array",
                     "value":[
                        {
                           "name":"原用餐時間",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"oldEatHour"
                        }
                     ],
                     "format":"n/a",
                     "id":"setValue"
                  },
                  "setVisible":{
                     "name":"設定欄位是否顯示",
                     "type":"array",
                     "value":[
                        {  --kevin 補上資料
                           "name":"原用餐時間",
                           "type":"boolean",
                           "value":false,
                           "format":"N/A",
                           "id":"oldEatHour"
                        }
                     ],
                     "format":"n/a",
                     "id":"setVisible"
                  }
               },
               "format":"n/a",
               "id":"actions"
            }
         },
         "format":"n/a",
         "id":"verifyResult"
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
