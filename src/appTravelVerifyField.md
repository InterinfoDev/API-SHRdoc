# appTravelVerifyField
出差畫面欄位檢核，之後若其他功能有需要用到欄位檢核也會依照此格式回傳，主要會傳入欲檢核的欄位名稱以及畫面上所有欄位的資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelVerifyField
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
| request | {'fieldName':'startDate', 'empid':'admin', 'startDate':'20240508', 'endDate':'20240509', 'startTime':'0830', 'endTime':'1700' , 'isHoliday':false} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "fieldName":"startDate",
      "empid":"admin", 
      "startDate":"20240508",    
      "endDate":"20240509",     
      "startTime":"0830",        
      "endTime":"1700",
      "isHoliday":false
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
| fieldName | startDate | String | 欄位名稱 | Y | n/a |
| empid | admin | String | 員工編號 | N | n/a |
| startDate | 20240508 | String | 起始日期 | N | YYYYmmdd |
| endDate | 20240509 | String | 結束日期 | N | YYYYmmdd |    
| startTime | 0830 | String | 起始時間 | N | HHmm |  
| endTime | 1730 | String | 結束時間 | N | HHmm |
| isHoliday | false | boolean | 是否包含假日 | N | n/a |

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
                           "name":"出差總計",
                           "type":"string",
                           "value":"16.0",
                           "format":"hour",
                           "id":"amt"
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
            "hour":"小時",
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
