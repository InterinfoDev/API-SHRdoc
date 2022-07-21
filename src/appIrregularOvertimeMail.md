# appIrregularOvertimeMail
加班異常寄信

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimeMail
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
| request | {empid:[admin], companyId:TW, irragularYM:202207, viewType:A, beforeMins:30, afterMins:30, outMins:30, buttonKey:sentMailToEmployee, errorDate:[20220701] | Object |

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
       "empid":["admin"],
       "companyId":"TW",
       "irragularYM":"202207",
       "viewType":"A",
       "beforeMins":30,
       "afterMins":30,
       "outMins":30,
       "buttonKey":"sentMailToEmployee",
       "errorDate":["20220701"]
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
| empid | admin | Vector(String) | 員工編號 | Y | n/a |
| companyId | TW | String | 公司代號 | Y | n/a |
| irragularYM | 202207 | String | 查詢年月 | Y | AC(YYYYmm) |
| viewType | A | String | 顯示種類 | Y | n/a |
| beforeMins | 30 | Integer | 提前多久刷卡視為異常 | Y | n/a |
| afterMins | 30 | Integer | 延後多久刷卡視為異常 | Y | n/a |
| outMins | 30 | Integer | 刷卡時間超過多久未報加班視為異常 | Y | n/a |
| buttonKey | sentMailToEmployee | String | 進信給自己或主管 | Y | n/a |
| errorDate | 20220701 | String | 當筆資料的key值(日期) | Y | AC(YYYYmmdd) |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "異動成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "MessageInfor":{
         "name":"寄信資訊",
         "type":"object",
         "value":{
            "sendResult":{
               "name":"寄信結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"sendResult"
            },
            "sendMessage":{
               "name":"寄信訊息",
               "type":"string",
               "value":"寄發mail完成，應寄發：1筆 失敗：0筆",
               "format":"n/a",
               "id":"sendMessage"
            }
         },
         "format":"n/a",
         "id":"MessageInfor"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "查無資料"
    ],
    "data": {}
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
