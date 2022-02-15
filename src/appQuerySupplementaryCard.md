# appQuerySupplementaryCard
取得補卡資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQuerySupplementaryCard
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
| request | {eventYM:202111, eventStartDate:20211101, eventEndDate:20211130, eventDate:20211130} | Object | 查詢條件

### JSON representation
Case 1 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cardStartDate":"20210603",
        "cardEndDate":"20220302",
        "empid":"",
        "depNumber":[]
    }
}
```
Case 2 . Here is a JSON representation of request. 
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cardYM":"2021906"
        "empid":"",
        "depNumber":[]
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
| Case No | Key | Value | Type | Description | Required | Format |
|:----------|:----------|:-------------|:-----|:------------|:------------|:------------|
|   | empid | admin | String | 員工編號 | N | n/a | 查詢員工編號 |
|   | depNumber | [5] | Array(Integer) | 部門代號 | N | n/a |
|   | state | false | boolean | 是否生效 | N | 已生效:true、未生效:false、全部:不放此欄位|
| 1 | cardStartDate | 20210601 | String | 查詢日期(起) | Y | AC(YYYYmmdd) |
|   | cardEndDate | 20220315 | String | 查詢日期(迄) | Y | AC(YYYYmmdd) |
| 2 | cardYM | 202106 | String | 查詢年月 | Y | AC(YYYYmm) |

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
      "supplementaryCard":{
         "name":"補卡資訊",
         "type":"array",
         "value":[
            {
               "name":"補卡明細",
               "type":"object",
               "value":{
                  "addDate":{
                     "name":"申請日期",
                     "type":"string",
                     "value":"20210610",
                     "format":"YYYYmmdd",
                     "id":"addDate"
                  },
                  "file":{
                     "name":"附件檔案",
                     "type":"string",
                     "value":{
                        "fileType":{
                           "name":"檔案類型",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"fileType"
                        },
                        "fileUrl":{
                           "name":"檔案路徑",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"fileUrl"
                        },
                        "fileName":{
                           "name":"檔案名稱",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"fileName"
                        }
                     },
                     "format":"n/a",
                     "id":"file"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
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
                     "value":"20210610",
                     "format":"YYYYmmdd",
                     "id":"cardDate"
                  },
                  "cardTime":{
                     "name":"補卡時間",
                     "type":"string",
                     "value":"0830",
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
                  "depCode":{
                     "name":"部門明碼",
                     "type":"string",
                     "value":"14121",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"supplementaryCardDetail"
            },
            {
               "name":"補卡明細",
               "type":"object",
               "value":{
                  "addDate":{
                     "name":"申請日期",
                     "type":"string",
                     "value":"20210806",
                     "format":"YYYYmmdd",
                     "id":"addDate"
                  },
                  "file":{
                     "name":"附件檔案",
                     "type":"string",
                     "value":{
                        "fileType":{
                           "name":"檔案類型",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"fileType"
                        },
                        "fileUrl":{
                           "name":"檔案路徑",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"fileUrl"
                        },
                        "fileName":{
                           "name":"檔案名稱",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"fileName"
                        }
                     },
                     "format":"n/a",
                     "id":"file"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"applytest001",
                     "format":"n/a",
                     "id":"empid"
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
                     "value":"20210802",
                     "format":"YYYYmmdd",
                     "id":"cardDate"
                  },
                  "cardTime":{
                     "name":"補卡時間",
                     "type":"string",
                     "value":"0800",
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
                     "value":"單O申",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "depCode":{
                     "name":"部門明碼",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"approved"
                  }
               },
               "format":"n/a",
               "id":"supplementaryCardDetail"
            }
         ],
         "format":"n/a",
         "id":"supplementaryCard"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "supplementaryCard": {
            "name": "補卡資訊",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "supplementaryCard"
        },
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "YYYYmmdd": "西元年月日",
                "n/a": ""
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
