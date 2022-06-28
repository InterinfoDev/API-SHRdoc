# appOvertimeAdd
新增實際加班單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeAdd
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
| request | {{'empid':'9912011', 'overplanPno':'', 'startDate':'20220711', 'startTime':'2100', 'endTime':'2300', 'reason':'kevin中文實際加班單測試', 'payType':'B', 'overtimeDepartment':'9', 'allowanceClass':'', 'overtimeType':'A', 'totalPayHour':2.0, 'totalRestHour':0.0, 'specifyHour':0.0, 'oldEatHour':0.0, 'isEat':true, 'beforeWork':false, 'naturalDisaster':false, 'earlyLeave':false, 'misAmt':0, 'eatCount':0, 'oldEatCount':0, 'file':[{'fileName':'kevin.jpg','fileData':'xxx'}} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"9912011", 
      "overplanPno":"",
      "startDate":"20220711",
      "startTime":"2100",    
      "endTime":"2300",      
      "reason":"kevin中文實際加班單測試",   
      "overtimeType":"A",
      "overtimeDepartment":"9",
      "payType":"B",
      "allowanceClass":"",
      "totalPayHour":2.0,
      "totalRestHour":0.0,
      "specifyHour":0.0,
      "oldEatHour":0.0,
      "isEat":true,
      "earlyLeave":false,
      "naturalDisaster":false,
      "beforeWork":false,
      "misAmt":0,
      "eatCount":0,
      "oldEatCount":0,
      "file":[{
        "fileName":"kevin.jpg",
        "fileData":"base64"
      }]
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
| empid | admin | String | 員工編號 | Y | n/a |
| startDate | 20220527 | String | 起始日期 | Y | YYYYmmdd |
| startTime | 1900 | String | 起始時間 | Y | HHmm |  
| endTime | 2300 | String | 結束時間 | Y | HHmm |         
| reason | 20220524kevinOverplanTest | String | 加班內容 | Y | n/a |
| payType | A | String | 給付方式 | Y | n/a |
| allowanceClass |  | String | 津貼班別 | Y | n/a |
| overtimeDepartment | 9 | String | 加班部門 | Y | n/a |
| overtimeType | A | String | 加班類別 | Y | n/a |
| totalPayHour | 0.0 | Decimal | 總計給薪時數 | Y | hour | 
| totalRestHour | 0.0 | Decimal | 總計補休時數 | Y | hour |
| specifyHour | 0.0 | Decimal | 指定用餐時間 | Y | hour |
| oldEatHour | 0.0 | Decimal | 原用餐時間 | Y | hour |
| isEat | false | boolean | 是否用餐 | Y | n/a | 
| beforeWork | false | boolean | 跨日往前加班 | Y | n/a | 
| naturalDisaster | false | boolean | 天災 | Y | n/a | 
| earlyLeave | false | boolean | 申請提早退勸 | Y | n/a | 
| misAmt | 0 | integer | 誤餐費 | Y | currency | 
| eatCount | 0 | integer | 新用餐次數 | Y | count | 
| oldEatCount | 0 | integer | 原用餐次數 | Y | count | 
| file |  | String | 附件檔案 |  | n/a |
| fileName | test.jpg | String | 附件檔案 | N | n/a |
| fileData |  | String | 附件檔案 | N | base64 |

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
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "addOvertime":{
         "name":"新增實際加班單",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"單據W002022062800003已進入簽核流程，謝謝",
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
         "id":"addOvertime"
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
