# appVacationAdd
員工請假

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationAdd
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
| request | {'empid':'admin', 'vacationCode':'000', 'startDate':'20220429', 'endDate':'20220429', 'startTime':'0830', 'endTime':'1700', 'reason':'kevin中文測試', 'delayReason':'', 'jobAgent':'10900015', 'specialDate':'', 'isHoliday':false, 'planeTicket':0, 'flowAgent':'10900015', 'flowAgent1':'10900015', 'flowAgent2':'10900015', 'flowAgent3':'10900015', 'file':[{'fileName':'kevin.jpg','fileData':'base64'}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin", 
      "vacationCode":"000",
      "startDate":"20220429",  --kevin 改成startDate
      "endDate":"20220429",    --kevin 改成endDate
      "startTime":"0830",      --kevin 改成startTime
      "endTime":"1700",        --kevin 改成endTime
      "reason":"kevin中文測試",
      "delayReason":"",
      "jobAgent":"10900015",
      "specialDate":"",
      "isHoliday":false,
      "planeTicket":0,
      "flowAgent":"10900015",
      "flowAgent1":"10900015",   --kevin 改成flowAgent1
      "flowAgent2":"10900015",   --kevin 改成flowAgent2
      "flowAgent3":"10900015",   --kevin 改成flowAgent3
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
| vacationCode | 000 | String | 假別代碼 | Y | n/a |
| startDate | 20220429 | String | 起始日期 | Y | YYYYmmdd |
| endDate | 20220429 | String | 結束日期 | Y | YYYYmmdd |
| startTime | 0830 | String | 起始時間 | Y | HHmm |
| endTime | 1700 | String | 結束時間 | Y | HHmm |
| reason | kevin中文測試 | String | 請假說明 | Y | n/a |
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
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "addVacation":{
         "name":"新增請假單",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"單據W00202204290004已進入簽核流程，謝謝",
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
