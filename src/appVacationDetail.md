# appVacationDetail
查詢該假單詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationDetail
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
| request | {pno:W00202201250001, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的假單單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "pno":"W00202201250001", 
        "empid":"admin"
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
| pno | W00202201250001 | String | 單據編號 | Y | n/a |
| empid | admin | String | 員工編號 | Y | n/a |


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
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "day":"天",
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
               "value":"225721252929321375615416977232747178356918537416530009027085451609431956050312520400829159686808175296041432946124037",
               "format":"n/a",
               "id":"historyKey"
            }
         },
         "format":"n/a",
         "id":"flowHistory"
      },
      "vacationDetail":{
         "name":"假單詳細資訊",
         "type":"object",
         "value":{
            "isHoliday":{           --kevin 新增欄位isHoliday
               "name":"是否包含假日",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"isHoliday"
            },
            "jobAgent":{               --kevin 改名jobAgent
               "name":"職務代理人",
               "type":"object",
               "value":{
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"薪O條",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"11000021",
                     "format":"n/a",
                     "id":"empid"
                  }
               },
               "format":"n/a",
               "id":"jobAgent"          --kevin 改名jobAgent
            },
            "total":{                   --kevin 改名total
               "name":"總計",
               "type":"decimal",
               "value":8.0,
               "format":"hour",
               "id":"total"             --kevin 改名total
            },
            "vacationStartTime":{        --kevin 改名vacationStartTime
               "name":"起始時間",
               "type":"string",
               "value":"0800",
               "format":"HHmm",
               "id":"vacationStartTime"  --kevin 改名vacationStartTime
            },
            "vacationName":{          --kevin 改名vacationName
               "name":"假別名稱",
               "type":"string",
               "value":"休息",
               "format":"n/a",
               "id":"vacationName"    --kevin 改名vacationName
            },
            "pno":{
               "name":"單據編號",
               "type":"string",
               "value":"W00202201250001",
               "format":"n/a",
               "id":"pno"
            },
            "vacationStartDate":{           --kevin 改名vacationStartDate
               "name":"起始日期",
               "type":"string",
               "value":"20220117",
               "format":"YYYYmmdd",
               "id":"vacationStartDate"     --kevin 改名vacationStartDate
            },
            "uploadFiles":{
               "name":"附件資訊",
               "type":"array",
               "value":[
                  {
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
                        "value":"97922998003575924465",
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
                  {
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
                        "value":"97922998003575924465",
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
                  {
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
                        "value":"97922998003575924465",
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
                  }
               ],
               "format":"n/a",
               "id":"uploadFiles"
            },
            "planeTicket":{         --kevin新增欄位planeTicket
               "name":"機票",
               "type":"integer",
               "value":0,
               "format":"ticket",
               "id":"planeTicket"   
            },
            "flowAgent":{           --kevin改名flowAgent
               "name":"簽核代理人",
               "type":"array",
               "value":[
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  },
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  },
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  },
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  }
               ],
               "format":"n/a",
               "id":"flowAgent"         --kevin 改名flowAgent
            },
             "vacationEndTime":{         --kevin 改名vacationEndTime
               "name":"結束時間",
               "type":"string",
               "value":"1700",
               "format":"HHmm",
               "id":"vacationEndTime"    --kevin 改名vacationEndTime
            },
            "vacationEndDate":{          --kevin 改名vacationEndDate
               "name":"結束日期",
               "type":"string",
               "value":"20220117",
               "format":"YYYYmmdd",
               "id":"vacationEndDate"     --kevin 改名vacationEndDate
            },
            "reason":{                          --kevin 改名reason
               "name":"請假原因",                --kevin 改名請假原因
               "type":"string",
               "value":"20220125KevinTestTest",
               "format":"n/a",
               "id":"reason"                    --kevin 改名reason
            },
            "companyFullName":{
               "name":"公司全名",
               "type":"string",
               "value":"72英特內全名(中和)",
               "format":"n/a",
               "id":"companyFullName"
            },
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系O管",
               "format":"n/a",
               "id":"empFullName"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
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
            }
            "delayReason":{             --kevin 改名delayReason
               "name":"逾期請假原因",
               "type":"string",
               "value":"20220125KevinTestTestLateLate",
               "format":"n/a",
               "id":"delayReason"       --kevin 改名delayReason
            },
            "specialDate":{
               "name":"特殊日期",
               "type":"string",
               "value":"",
               "format":"YYYYmmdd",
               "id":"spectialDate"
            },
         },
         "format":"n/a",
         "id":"vacationDetail"
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
