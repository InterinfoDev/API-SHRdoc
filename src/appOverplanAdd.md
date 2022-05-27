# appOverplanAdd
新增預定加班單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOverplanAdd
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
| request | {{'empid':'admin', 'startDate':'20220527', 'startTime':'1900', 'endTime':'2200', 'reason':'xxx', 'payType':'A', 'totalPayHour':0.0, 'totalRestHour':0.0, 'specifyHour':0.0, 'oldEatHour':0.0, 'isEat':false, 'beforeWork':false, 'file':[{'fileName':'kevin.jpg','fileData':'base64'}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
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
      "beforeWork":false,
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
| reason | 20220524kevinOverplanTest | String | 請假說明 | N | n/a |
| payType | A | String | 給付方式 | Y | n/a |
| totalPayHour | 0.0 | Decimal | 總計給薪時數 | Y | hour | 
| totalRestHour | 0.0 | Decimal | 總計補休時數 | Y | hour |
| specifyHour | 0.0 | Decimal | 指定用餐時間 | Y | hour |
| oldEatHour | 0.0 | Decimal | 原用餐時間 | Y | hour |
| isEat | false | boolean | 是否用餐 | Y | n/a | 
| beforeWork | false | boolean | 跨日往前加班 | Y | n/a | 
| file |  | String | 附件檔案 |  | n/a |
| fileName | test.jpg | String | 附件檔案 | N | n/a |
| fileData |  | String | 附件檔案 | N | base64 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "addOverplan":{
         "name":"新增預定加班單",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"單據W002022052600001已進入簽核流程，謝謝",
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
         "id":"addVacation"
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
