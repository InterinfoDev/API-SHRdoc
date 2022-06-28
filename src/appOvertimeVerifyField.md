# appOvertimeVerifyField
實際加班單畫面欄位檢核

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeVerifyField
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
| request | {{'fieldName':'startTime','empid':'9912011','startDate':'20220712','startTime':'2100','endTime':'2300','reason':'ttt','payType':'B','totalPayHour':0.0,'totalRestHour':0.0,'specifyHour':0.0,'eatCount':0,'isEat':true,'beforeWork':false, 'naturalDisaster':false, 'earlyLeave':false, 'overplanPno':'W002022062700011', 'overtimeType':'A', 'overtimeDepartment':'9'}} | Object | 異動條件

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
      "overplanPno":'W002022062700011',
      "overtimeType":"A",
      "overtimeDepartment":"9",
      "payType":"A",          
      "totalPayHour":0.0,
      "totalRestHour":0.0,
      "specifyHour":0.0,
      "eatCount":0,
      "isEat":false,
      "earlyLeave":false,
      "naturalDisaster":false,
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
| reason | 20220524kevinOverplanTest | String | 加班內容 | N | n/a |
| payType | A | String | 給付方式 | N | n/a |
| overplanPno | W002022062700011 | String | 預定加班單號 | N | n/a |
| overtimeDepartment | 9 | String | 加班部門 | N | n/a |
| overtimeType | A | String | 加班類別 | N | n/a |
| totalPayHour | 0.0 | Decimal | 總計給薪時數 | N | hour | 
| totalRestHour | 0.0 | Decimal | 總計補休時數 | N | hour |
| specifyHour | 0.0 | Decimal | 指定用餐時間 | N | hour |
| eatCount | 0 | integer | 新用餐次數 | N | count |
| isEat | false | boolean | 是否用餐 | N | n/a | 
| beforeWork | false | boolean | 跨日往前加班 | N | n/a | 
| naturalDisaster | false | boolean | 天災 | N | n/a | 
| earlyLeave | false | boolean | 申請提早退勸 | N | n/a | 

### Using Field
| FieldName | Description |
|:---------|:-----|
| startTime | 起始時間 |
| endTime | 結束時間 |
| payType | 給付方式 |
| isEat | 是否用餐 |

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
                        
                     ],
                     "format":"n/a",
                     "id":"setEditable"
                  },
                  "setValue":{
                     "name":"設定欄位值",
                     "type":"array",
                     "value":[
                        {
                           "name":"平日第一段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"dailyRate1"
                        },
                        {
                           "name":"平日第二段倍率時數",
                           "type":"decimal",
                           "value":2.0,
                           "format":"hour",
                           "id":"dailyRate2"
                        },
                        {
                           "name":"平日第三段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"dailyRate3"
                        },
                        {
                           "name":"平日第四段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"dailyRate4"
                        },
                        {
                           "name":"假日第一段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"holidayRate1"
                        },
                        {
                           "name":"假日第二段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"holidayRate2"
                        },
                        {
                           "name":"假日第三段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"holidayRate3"
                        },
                        {
                           "name":"假日第四段倍率時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"holidayRate4"
                        },
                        {
                           "name":"誤餐費",
                           "type":"integer",
                           "value":0,
                           "format":"currency",
                           "id":"misAmt"
                        },
                        {
                           "name":"新用餐次數",
                           "type":"integer",
                           "value":0,
                           "format":"count",
                           "id":"eatCount"
                        },
                        {
                           "name":"原用餐次數",
                           "type":"integer",
                           "value":0,
                           "format":"count",
                           "id":"oldEatCount"
                        },
                        {
                           "name":"原用餐時間",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"oldEatHour"
                        },
                        {
                           "name":"總計補休時數",
                           "type":"decimal",
                           "value":0.0,
                           "format":"hour",
                           "id":"totalRestHour"
                        },
                        {
                           "name":"總計給薪時數",
                           "type":"decimal",
                           "value":2.0,
                           "format":"hour",
                           "id":"totalPayHour"
                        }
                     ],
                     "format":"n/a",
                     "id":"setValue"
                  },
                  "setVisible":{
                     "name":"設定欄位是否顯示",
                     "type":"array",
                     "value":[
                        
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
            "currency":"元",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "count":"數量",
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
