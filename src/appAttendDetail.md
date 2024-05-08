# appAttendDetail
取得指定年月、員工考勤詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAttendDetail
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {attendYM:202104, empid:admin} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "attendYM":"202104", 
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
| attendYM | 202104 | String | 考勤年月 | Y | AC(YYYYmm) |
| empid | admin | String | 員工編號 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "id":"main", --lucas 修改為main
         "name":"考勤資訊列表",
         "value":{
            "ym":{
               "id":"ym",
               "name":"考勤年月",
               "value":"202110",
               "type":"string",
               "format":"YYYYmm"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "attend":{
         "id":"attend", --lucas修改
         "name":"考勤資訊",
         "value":[
            {
               "id":"20211001",
               "name":"每天考勤明細",
               "value":{
                  "workDate":{
                     "id":"workDate",
                     "name":"出勤日期",
                     "value":"20211001",
                     "type":"string",
                     "format":"YYYYmmdd"  --lucas 修改YYYYmmdd
                  },
                  "workClass":{
                     "id":"workClass",
                     "name":"班別代號",
                     "value":"D",
                     "type":"string",
                     "format":"n/a"
                  },
                  "workClassName":{
                     "id":"workClassName",
                     "name":"班別名稱",
                     "value":"日常班",
                     "type":"string",
                     "format":"n/a"
                  },
                  "workOn":{
                     "id":"workOn",
                     "name":"上班時間",
                     "value":"0900",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "workOff":{
                     "id":"workOff",
                     "name":"下班時間",
                     "value":"1800",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "punchIn":{
                     "id":"punchIn",
                     "name":"進卡時間",
                     "value":"0854",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "punchOut":{
                     "id":"punchOut",
                     "name":"出卡時間",
                     "value":"1802",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "isAbnormal":{
                     "id":"isAbnormal",
                     "name":"是否考勤異常",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "haveLinkPermission":{
                     "id":"haveLinkPermission",
                     "name":"是否顯示補卡連結",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "isNextDay": {
                     "name": "是否跨日為出卡",
                     "type": "boolean",
                     "value": false,
                     "id": "isAbnormal",
                     "format": "n/a"
                  },
                  "abnormal":{
                     "id":"abnormal",
                     "name":"考勤異常說明",
                     "value":"遲到1分鐘",
                     "type":"string",
                     "format":"n/a"
                  },
                  "vacationInfo":{
                     "id":"vacationInfo",
                     "name":"請假說明",
                     "value":[
                        {
                           "vacationCode":{
                              "id":"vacationCode",
                              "name":"假別代號",
                              "value":"98",
                              "type":"string",
                              "format":"n/a"
                           },
                           "vacationName":{
                              "id":"vacationName",
                              "name":"假別名稱",
                              "value":"特休",
                              "type":"string",
                              "format":"n/a"
                           },
                           "vacationBeginTime":{
                              "id":"vacationBeginTime",
                              "name":"假別起始時間",
                              "value":"0900",
                              "type":"string",
                              "format":"HHmm"
                           },
                           "vacationEndTime":{
                              "id":"vacationEndTime",
                              "name":"假別結束時間",
                              "value":"1800",
                              "type":"string",
                              "format":"HHmm"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "overplanInfo":{
                     "id":"overplanInfo",
                     "name":"預定加班說明",
                     "value":[
                        {
                           "overplanBeginTime":{
                              "id":"overplanBeginTime",
                              "name":"預定加班起始時間",
                              "value":"1900",
                              "type":"string",
                              "format":"HHmm"
                           },
                           "overplanEndTime":{
                              "id":"overplanEndTime",
                              "name":"預定加班結束時間",
                              "value":"2300",
                              "type":"string",
                              "format":"HHmm"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "overtimeInfo":{
                     "id":"overtimeInfo",
                     "name":"加班說明",
                     "value":[
                        {
                           "overtimeBeginTime":{
                              "id":"overtimeBeginTime",
                              "name":"加班起始時間",
                              "value":"1900",
                              "type":"string",
                              "format":"HHmm"
                           },
                           "overtimeEndTime":{
                              "id":"overtimeEndTime",
                              "name":"加班結束時間",
                              "value":"2300",
                              "type":"string",
                              "format":"HHmm"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "repairPunch":{
                     "id":"repairPunch",
                     "name":"補刷說明",
                     "value":[
                        {
                           "repairPunchTime":{
                              "id":"repairPunchTime",
                              "name":"補刷時間",
                              "value":"0830",
                              "type":"string",
                              "format":"HHmm"
                           },
                           "repairPunchType":{
                              "id":"repairPunchType",
                              "name":"補刷類別",
                              "value":"進卡/出卡",
                              "type":"string",
                              "format":"n/a"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "noneApproved":{
                     "id":"noneApproved",
                     "name":"未生效單據",
                     "value":[
                        {
                           "formName":{
                              "id":"formName",
                              "name":"單據名稱",
                              "value":"請假單",
                              "type":"string",
                              "format":"n/a"
                           },
                           "formDescription":{
                              "id":"formDescription",
                              "name":"單據未完成說明",
                              "value":"09:00~18:00",
                              "type":"string",
                              "format":"n/a"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "overtimeError":{
                     "id":"overtimeError",
                     "name":"加班異常",
                     "value":{
                        "errorDescription":{
                           "id":"errorDescription",
                           "name":"異常類別",
                           "value":"私事處理",
                           "type":"string",
                           "format":"n/a"
                        }
                     },
                     "type":"object",
                     "format":"n/a"
                  },
                  "punchCardInfo":{
                     "id":"punchCardInfo",
                     "name":"刷卡明細",
                     "value":[
                        {
                           "punchTime":{
                              "id":"punchTime",
                              "name":"刷卡時間",
                              "value":"08:54",
                              "type":"string",
                              "format":"n/a"
                           }
                            "cardType": {
                              "name": "刷卡卡別",
                              "type": "string",
                              "value": "進",
                              "format": "n/a",
                              "id": "cardType"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  }
               }, --andy 格式寫錯,type和format應該在外面這層
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{--lucas 移除count
            "YYYYmm":"西元年月",
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分",
            "n/a":""
         }
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
