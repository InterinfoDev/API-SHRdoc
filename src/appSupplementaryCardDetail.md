# appSupplementaryCardDetail
查詢該補假詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardDetail
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
| request | {supplementaryCardKey:20210600000000000002} | Object | 查詢條件(依據使用者所選擇要查看的假單單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "supplementaryCardKey":"20210600000000000002"
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
| supplementaryCardKey | 20210600000000000002 | String | 單據編號 | Y | n/a |

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
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "flowHistory":{
         "name":"流程紀錄",
         "type":"object",
         "value":{
            "historyKey":{
               "name":"流程鍵值",
               "type":"string",
               "value":"3799391871311144335627777514617065132983803072298167159419265428929297071709253604564753867957635073218731940934947702912904196297242807",
               "format":"n/a",
               "id":"historyKey"
            }
         },
         "format":"n/a",
         "id":"flowHistory"
      },
      "supplementaryCardDetail":{
         "name":"補卡詳細資訊",
         "type":"object",
         "value":{
            "cardType":{
               "name":"進出別",
               "type":"string",
               "value":"其他",
               "format":"n/a",
               "id":"cardType"
            },
            "addDate":{
               "name":"申請日期",
               "type":"string",
               "value":"20210629",
               "format":"YYYYmmdd",
               "id":"addDate"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "approvalStatus":{
               "name":"簽核狀態",
               "type":"string",
               "value":"未生效",
               "format":"n/a",
               "id":"approvalStatus"
            },
            "uploadFiles":{
               "name":"附件資訊",
               "type":"array",
               "value":[
                  
               ],
               "format":"n/a",
               "id":"uploadFiles"
            },
            "reason":{
               "name":"補登原因",
               "type":"string",
               "value":"忘刷卡",
               "format":"n/a",
               "id":"reason"
            },
            "cardDate":{
               "name":"補卡日期",
               "type":"string",
               "value":"20210601",
               "format":"YYYYmmdd",
               "id":"cardDate"
            },
            "cardTime":{
               "name":"補卡時間",
               "type":"string",
               "value":"0600",
               "format":"HHmm",
               "id":"cardTime"
            },
            "note":{
               "name":"備註",
               "type":"string",
               "value":"忘刷卡",
               "format":"n/a",
               "id":"note"
            },
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系O管",
               "format":"n/a",
               "id":"empFullName"
            },
            "depFullName":{
               "name":"部門名稱",
               "type":"string",
               "value":"L1線A班",
               "format":"n/a",
               "id":"depFullName"
            },
            "empFullEname":{
               "name":"員工英文姓名",
               "type":"string",
               "value":"test_Ename",
               "format":"n/a",
               "id":"empFullEname"
            },
            "depCode":{
               "name":"部門代號",
               "type":"string",
               "value":"14121",
               "format":"n/a",
               "id":"depCode"
            }
         },
         "format":"n/a",
         "id":"supplementaryCardDetail"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
