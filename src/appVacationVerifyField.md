# appVacationVerifyField
請假畫面欄位檢核，之後若其他功能有需要用到欄位檢核也會依照此格式回傳，主要會傳入欲檢核的欄位名稱以及畫面上所有欄位的資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationVerifyField
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
| request | {'fieldName':'startDate', 'empid':'admin', 'vacationCode':'000', 'startDate':'20220429', 'endDate':'20220429', 'startTime':'0830', 'endTime':'1700', 'reason':'kevin中文測試', 'delayReason':'', 'jobAgent':'10900015', 'specialDate':'', 'isHoliday':false, 'planeTicket':0, 'flowAgent':'10900015', 'flowAgent1':'10900015', 'flowAgent2':'10900015', 'flowAgent3':'10900015', 'file':[{'fileName':'kevin.jpg','fileData':'base64'}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "fieldName":"vacationStartDate",
      "empid":"admin", 
      "vacationCode":"000",
      "startDate":"20220429",    --kevin 改成startDate
      "endDate":"20220429",      --kevin 改成endDate
      "startTime":"0830",        --kevin 改成startTime
      "endTime":"1700",          --kevin 改成endTime
      "reason":"kevin中文測試",
      "delayReason":"",
      "jobAgent":"10900015",
      "specialDate":"",
      "isHoliday":false,
      "planeTicket":0,
      "flowAgent":"10900015",
      "flowAgent1":"10900015",    --kevin 改成flowAgent1
      "flowAgent2":"10900015",    --kevin 改成flowAgent2
      "flowAgent3":"10900015",    --kevin 改成flowAgent3
      "file":[{   --kevin 檔案改成陣列
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
| fieldName | vacationStartDate | String | 欄位名稱 | Y | n/a |
| empid | admin | String | 員工編號 | N | n/a |
| vacationCode | 000 | String | 假別代碼 | N | n/a |
| startDate | 20220503 | String | 起始日期 | N | YYYYmmdd |
| endDate | 20220503 | String | 結束日期 | N | YYYYmmdd |    
| startTime | 0830 | String | 起始時間 | N | HHmm |  
| endTime | 1730 | String | 結束時間 | N | HHmm |         
| reason | kevin中文測試 | String | 請假說明 | N | n/a |
| delayReason |  | String | 逾時請假說明 | N | n/a |
| jobAgent | 10900015 | String | 職務代理人 | N | n/a | 
| specialDate |  | String | 特殊日期 | N | YYYYmmdd |
| isHoliday | false | boolean | 是否包含假日 | N | n/a |
| planeTicket | 0 | integer | 機票 | N | ticket |
| flowAgent | 10900015 | String | 簽核代理人 | N | n/a | 
| flowAgent1 | 10900015 | String | 代理人一 | N | n/a | 
| flowAgent2 | 10900015 | String | 代理人二 | N | n/a | 
| flowAgent3 | 10900015 | String | 代理人三 | N | n/a | 
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
      "verifyResult":{
         "name":"檢核結果",
         "type":"object",
         "value":{
            "tipMessage":{
               "name":"檢核訊息",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"tipMessage"
            },
            "actions":{
               "name":"異動欄位",
               "type":"object",
               "value":{
                  "setEditable":{
                     "name":"設定欄位可否編輯",
                     "type":"array",
                     "value":[
                        {
                           "name":"起始日期",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"startDate"   --kevin改名startDate
                        },
                        {
                           "name":"結束日期",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"endDate"  --kevin改名endDate
                        },
                        {
                           "name":"起始時間",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"startTime"   --kevin改名startTime
                        },
                        {
                           "name":"結束時間",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"endTime"  --kevin改名endTime
                        },
                        {
                           "name":"逾時請假原因",
                           "type":"boolean",
                           "value":false,
                           "format":"n/a",
                           "id":"delayReason"
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
                           "name":"起始日期",
                           "type":"string",
                           "value":"20220503",
                           "format":"YYYYmmdd",
                           "id":"startDate"   --kevin改名startDate
                        },
                        {
                           "name":"結束日期",
                           "type":"string",
                           "value":"20220503",
                           "format":"YYYYmmdd",
                           "id":"endDate"  --kevin改名endDate
                        },
                        {
                           "name":"起始時間",
                           "type":"string",
                           "value":"0830",
                           "format":"HHmm",
                           "id":"startTime"   --kevin改名startTime
                        },
                        {
                           "name":"結束時間",
                           "type":"string",
                           "value":"1730",
                           "format":"HHmm",
                           "id":"endTime"  --kevin改名endTime
                        }
                     ],
                     "format":"n/a",
                     "id":"setValue"
                  },
                  "setVisible":{
                     "name":"設定欄位是否顯示",
                     "type":"array",
                     "value":[
                        {
                           "name":"起始日期",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"startDate"   --kevin改名startDate
                        },
                        {
                           "name":"結束日期",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"endDate"  --kevin改名endDate
                        },
                        {
                           "name":"起始時間",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"startTime"   --kevin改名startTime
                        },
                        {
                           "name":"結束時間",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"endTime"  --kevin改名endTime
                        },
                        {
                           "name":"逾時請假原因",
                           "type":"boolean",
                           "value":true,
                           "format":"n/a",
                           "id":"delayReason"
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
