# appIrregularOvertimeList
取得加班異常列表資訊

(回傳值 星期都會以數字格式 ex:0(星期日、1(星期一)...))
(班別 顏色種類有: black、red)
(異常日期 顏色種類有: black、green、red)
### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimeList
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
| request | {empid:admin,companyId:TW,irregularYM:202207,viewType:A,beforeMins:30,afterMins:30,outMins:30} | Object |

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":["admin"],
        "companyId":"TW",
        "irregularYM":"202207",     -- richard 修改request key值 irregularYM
        "viewType":"A",
        "beforeMins":30,
        "afterMins":30,
        "outMins":30
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
| irregularYM | 202207 | String | 查詢年月 | Y | AC(YYYYmm) | 
| viewType | A | String | 顯示種類 | Y | n/a |
| beforeMins | 30 | Integer | 提前多久刷卡視為異常 | Y | n/a |
| afterMins | 30 | Integer | 延後多久刷卡視為異常 | Y | n/a |
| outMins | 30 | Integer | 刷卡時間超過多久未報加班視為異常 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"加班異常資訊",
         "type":"object",
         "value":{
            "beforeMins":{                  --richard 新增欄位  beforeMins
               "name":"提前多久刷卡視為異常",
               "type":"integer",
               "value":30,
               "format":"min",
               "id":"beforeMins"             --richard 新增欄位 beforeMins
            },
            "outMins":{                     --richard 新增欄位  outMins
               "name":"刷卡時間超過多久未報加班視為異常",
               "type":"integer",
               "value":30,
               "format":"min",
               "id":"outMins"                --richard 新增欄位  outMins
            },
            "afterMins":{                    --richard 新增欄位  afterMins
               "name":"延後多久刷卡視為異常",
               "type":"integer",
               "value":30,
               "format":"min",
               "id":"afterMins"               --richard 新增欄位  afterMins
            },
            "showType":{                      --richard 新增欄位  showType
               "name":"顯示種類",
               "type":"string",
               "value":"B",
               "format":"n/a",
               "id":"showType"                  --richard 新增欄位  showType
            },
            "irregularYM":{
               "name":"加班異常年月",
               "type":"string",
               "value":"202207",
               "format":"YYYYmm",
               "id":"irregularYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "appIrregularOvertimeList":{
         "name":"員工加班異常列表",
         "type":"array",
         "value":[
            {
               "name":"員工加班異常資訊",
               "type":"object",
               "value":{
                  "detailInfor":{
                     "name":"展開資料",
                     "type":"object",
                     "value":{
                        "workClassName":{
                           "name":"班別",
                           "type":"string",
                           "value":"早班(8-17)",
                           "format":"n/a",
                           "id":"workClassName"
                        },
                        "overtimeState":{
                           "name":"加班情況",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"overtimeState"
                        },
                        "inCard":{
                           "name":"進卡",
                           "type":"string",
                           "value":"0800",
                           "format":"HHmm",
                           "id":"inCard"
                        },
                        "empid":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"admin",
                           "format":"n/a",
                           "id":"empid"
                        },
                        "dayOfWeek":{
                           "name":"異常日期星期",
                           "type":"integer",
                           "value":5,
                           "format":"n/a",
                           "id":"dayOfWeek"
                        },
                        "errorReason":{
                           "name":"異常說明",
                           "type":"string",
                           "value":"刷卡時間 0800 1838,異常原因,刷卡時間往後%1分鐘,未報加班",
                           "format":"n/a",
                           "id":"errorReason"
                        },
                        "classStartTime":{
                           "name":"班別時間(起)",
                           "type":"string",
                           "value":"0800",
                           "format":"HHmm",
                           "id":"classStartTime"
                        },
                        "unApproved":{
                           "name":"未簽核加班單",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"unApproved"
                        },
                        "classEndTime":{
                           "name":"班別時間(迄)",
                           "type":"string",
                           "value":"1700",
                           "format":"HHmm",
                           "id":"classEndTime"
                        },
                        "dayOfWeekColor":{
                           "name":"異常日期顏色",
                           "type":"string",
                           "value":"black",
                           "format":"n/a",
                           "id":"dayOfWeekColor"
                        },
                        "errorRespone":{
                           "name":"異常回應",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"errorRespone"
                        },
                        "outCard":{
                           "name":"出卡",
                           "type":"string",
                           "value":"1838",
                           "format":"HHmm",
                           "id":"outCard"
                        },
                        "classColor":{
                           "name":"班別顏色",
                           "type":"string",
                           "value":"black",
                           "format":"n/a",
                           "id":"classColor"
                        },
                        "empFullName":{
                           "name":"員工姓名",
                           "type":"string",
                           "value":"系統管理員",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "depFullName":{
                           "name":"部門名稱",
                           "type":"string",
                           "value":"英特內股份有限公司",
                           "format":"n/a",
                           "id":"depFullName"
                        },
                        "errorDate":{
                           "name":"異常日期",
                           "type":"string",
                           "value":"20220701",
                           "format":"YYYYmmdd",
                           "id":"errorDate"
                        },
                        "depCode":{
                           "name":"部門代號",
                           "type":"string",
                           "value":"99999",
                           "format":"n/a",
                           "id":"depCode"
                        },
                        "editable": {              --richard 新增欄位 editable
                            "name": "可異動資料",
                            "type": "boolean",
                            "value": false,
                            "format": "n/a",
                            "id": "editable"       --richard 新增欄位 editable
                        },
                        "mdate": {
                             "name": "異動日期",
                             "type": "string",
                             "value": "20231123",
                             "format": "YYYYmmdd",
                             "id": "mdate"
                         },
                         "muser": {
                             "name": "異動人",
                             "type": "string",
                             "value": "吳兵千",
                             "format": "n/a",
                             "id": "muser"
                        },
                         "mtime": {
                              "name": "異動時間",
                              "type": "string",
                              "value": "172057",
                              "format": "n/a",
                              "id": "mtime"
                        }
                     },
                     "format":"n/a",
                     "id":"detailInfor"
                  },
                  "simpleInfor":{
                     "name":"簡易資料",
                     "type":"object",
                     "value":{
                        "simpleDayOfWeekColor":{
                           "name":"異常日期顏色",
                           "type":"string",
                           "value":"black",
                           "format":"n/a",
                           "id":"simpleDayOfWeekColor"
                        },
                        "simpleErrorDate":{
                           "name":"異常日期",
                           "type":"string",
                           "value":"20220701",
                           "format":"YYYYmmdd",
                           "id":"simpleErrorDate"
                        },
                        "simpleErrorReason":{
                           "name":"異常說明",
                           "type":"string",
                           "value":"刷卡時間 0800 1838,異常原因,刷卡時間往後%1分鐘,未報加班",
                           "format":"n/a",
                           "id":"simpleErrorReason"
                        },
                        "simpleInCard":{
                           "name":"進卡",
                           "type":"string",
                           "value":"0800",
                           "format":"HHmm",
                           "id":"simpleInCard"
                        },
                        "simpleDayOfWeek":{
                           "name":"異常日期星期",
                           "type":"integer",
                           "value":5,
                           "format":"dayofweek",
                           "id":"simpleDayOfWeek"
                        },
                        "simpleOutCard":{
                           "name":"出卡",
                           "type":"string",
                           "value":"1838",
                           "format":"HHmm",
                           "id":"simpleOutCard"
                        }
                     },
                     "format":"n/a",
                     "id":"simpleInfor"
                  }
               },
               "format":"n/a",
               "id":"IrregularOvertimeInformation"
            },
            {
               "name":"員工加班異常資訊",
               "type":"object",
               "value":{
                  "detailInfor":{
                     "name":"展開資料",
                     "type":"object",
                     "value":{
                        "workClassName":{
                           "name":"班別",
                           "type":"string",
                           "value":"例假日",
                           "format":"n/a",
                           "id":"workClassName"
                        },
                        "overtimeState":{
                           "name":"加班情況",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"overtimeState"
                        },
                        "inCard":{
                           "name":"進卡",
                           "type":"string",
                           "value":"",
                           "format":"HHmm",
                           "id":"inCard"
                        },
                        "empid":{
                           "name":"員工編號",
                           "type":"string",
                           "value":"admin",
                           "format":"n/a",
                           "id":"empid"
                        },
                        "dayOfWeek":{
                           "name":"異常日期星期",
                           "type":"integer",
                           "value":0,
                           "format":"n/a",
                           "id":"dayOfWeek"
                        },
                        "errorReason":{
                           "name":"異常說明",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"errorReason"
                        },
                        "classStartTime":{
                           "name":"班別時間(起)",
                           "type":"string",
                           "value":"",
                           "format":"HHmm",
                           "id":"classStartTime"
                        },
                        "unApproved":{
                           "name":"未簽核加班單",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"unApproved"
                        },
                        "classEndTime":{
                           "name":"班別時間(迄)",
                           "type":"string",
                           "value":"",
                           "format":"HHmm",
                           "id":"classEndTime"
                        },
                        "dayOfWeekColor":{
                           "name":"異常日期顏色",
                           "type":"string",
                           "value":"red",
                           "format":"n/a",
                           "id":"dayOfWeekColor"
                        },
                        "errorRespone":{
                           "name":"異常回應",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"errorRespone"
                        },
                        "outCard":{
                           "name":"出卡",
                           "type":"string",
                           "value":"",
                           "format":"HHmm",
                           "id":"outCard"
                        },
                        "classColor":{
                           "name":"班別顏色",
                           "type":"string",
                           "value":"red",
                           "format":"n/a",
                           "id":"classColor"
                        },
                        "empFullName":{
                           "name":"員工姓名",
                           "type":"string",
                           "value":"系統管理員",
                           "format":"n/a",
                           "id":"empFullName"
                        },
                        "depFullName":{
                           "name":"部門名稱",
                           "type":"string",
                           "value":"英特內股份有限公司",
                           "format":"n/a",
                           "id":"depFullName"
                        },
                        "errorDate":{
                           "name":"異常日期",
                           "type":"string",
                           "value":"20220731",
                           "format":"YYYYmmdd",
                           "id":"errorDate"
                        },
                        "depCode":{
                           "name":"部門代號",
                           "type":"string",
                           "value":"99999",
                           "format":"n/a",
                           "id":"depCode"
                        }
                     },
                     "format":"n/a",
                     "id":"detailInfor"
                  },
                  "simpleInfor":{
                     "name":"簡易資料",
                     "type":"object",
                     "value":{
                        "simpleDayOfWeekColor":{
                           "name":"異常日期顏色",
                           "type":"string",
                           "value":"red",
                           "format":"n/a",
                           "id":"simpleDayOfWeekColor"
                        },
                        "simpleErrorDate":{
                           "name":"異常日期",
                           "type":"string",
                           "value":"20220731",
                           "format":"YYYYmmdd",
                           "id":"simpleErrorDate"
                        },
                        "simpleErrorReason":{
                           "name":"異常說明",
                           "type":"string",
                           "value":"",
                           "format":"n/a",
                           "id":"simpleErrorReason"
                        },
                        "simpleInCard":{
                           "name":"進卡",
                           "type":"string",
                           "value":"",
                           "format":"HHmm",
                           "id":"simpleInCard"
                        },
                        "simpleDayOfWeek":{
                           "name":"異常日期星期",
                           "type":"integer",
                           "value":0,
                           "format":"dayofweek",
                           "id":"simpleDayOfWeek"
                        },
                        "simpleOutCard":{
                           "name":"出卡",
                           "type":"string",
                           "value":"",
                           "format":"HHmm",
                           "id":"simpleOutCard"
                        }
                     },
                     "format":"n/a",
                     "id":"simpleInfor"
                  }
               },
               "format":"n/a",
               "id":"IrregularOvertimeInformation"
            }
         ],
         "format":"n/a",
         "id":"appIrregularOvertimeList"
      },
      "employee":{
         "name":"員工基本資料",
         "type":"object",
         "value":{
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系統管理員",
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
            "empFullEname":{
               "name":"員工英文姓名",
               "type":"string",
               "value":"Administrator",
               "format":"n/a",
               "id":"empFullEname"
            }
         },
         "format":"n/a",
         "id":"employee"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "dayofweek":"星期"
         }
      },
      "responseList": {                 --richard 新增欄位 responseList
            "name": "異常回報下拉清單",
            "type": "object",
            "value": [
                {
                    "responseName": {            --richard 新增 responseName
                        "name": "異常原因",
                        "type": "string",
                        "value": "測試4",
                        "format": "n/a",
                        "id": "responseName"    --richard 新增欄位 responseName
                    },
                    "responseCode": {           --richard 新增欄位 responseCode
                        "name": "異常代碼",
                        "type": "string",
                        "value": "A04",
                        "format": "n/a",
                        "id": "responseCode"     --richard 新增欄位 responseCode
                    },
                    "responseReason": {          --richard 新增欄位 responseReason
                        "name": "備註",
                        "type": "string",
                        "value": "",
                        "format": "n/a",
                        "id": "responseReason"  --richard 新增欄位 responseReason
                    }
                },
                {
                    "responseName": {           
                        "name": "異常原因",
                        "type": "string",
                        "value": "測試3",
                        "format": "n/a",
                        "id": "responseName"
                    },
                    "responseCode": {
                        "name": "異常代碼",
                        "type": "string",
                        "value": "A03",
                        "format": "n/a",
                        "id": "responseCode"
                    },
                    "responseReason": {
                        "name": "備註",
                        "type": "string",
                        "value": "",
                        "format": "n/a",
                        "id": "responseReason"
                    }
                },
                {
                    "responseName": {
                        "name": "異常原因",
                        "type": "string",
                        "value": "測試1",
                        "format": "n/a",
                        "id": "responseName"
                    },
                    "responseCode": {
                        "name": "異常代碼",
                        "type": "string",
                        "value": "A01",
                        "format": "n/a",
                        "id": "responseCode"
                    },
                    "responseReason": {
                        "name": "備註",
                        "type": "string",
                        "value": "",
                        "format": "n/a",
                        "id": "responseReason"
                    }
                }
            ],
        "format": "n/a",
        "id": "responseList"        --richard 新增欄位 responseList
      },
      "editableButton":{
         "name":"可使用功能按鈕資訊",
         "type":"object",
         "value":{
            "buttonList":{
               "name":"按鈕清單",
               "type":"object",
               "value":[
                  {
                    "buttonName": {
                        "name": "按鈕名稱",
                        "type": "string",
                        "value": "通知員工本人",
                        "format": "n/a",
                        "id": "buttonName"
                    },
                    "buttonId": {
                        "name": "按鈕ID",
                        "type": "string",
                        "value": "sentMailToEmployee",
                        "format": "n/a",
                        "id": "buttonId"
                    }
                },
                {
                    "buttonName": {
                        "name": "按鈕名稱",
                        "type": "string",
                        "value": "通知第一層主管",
                        "format": "n/a",
                        "id": "buttonName"
                    },
                    "buttonId": {
                        "name": "按鈕ID",
                        "type": "string",
                        "value": "sentMailToSupervisor",
                        "format": "n/a",
                        "id": "buttonId"
                    }
                },
                {
                    "buttonName": {
                        "name": "按鈕名稱",
                        "type": "string",
                        "value": "查閱加班異常寄發名單",
                        "format": "n/a",
                        "id": "buttonName"
                    },
                    "buttonId": {
                        "name": "按鈕ID",
                        "type": "string",
                        "value": "selectIrregularList",
                        "format": "n/a",
                        "id": "buttonId"
                    }
                },
                {
                    "buttonName": {
                        "name": "按鈕名稱",
                        "type": "string",
                        "value": "下載員工異常名單",
                        "format": "n/a",
                        "id": "buttonName"
                    },
                    "buttonId": {
                        "name": "按鈕ID",
                        "type": "string",
                        "value": "downLoadIrregularList",
                        "format": "n/a",
                        "id": "buttonId"
                    }
                },
                {
                    "buttonName": {
                        "name": "按鈕名稱",
                        "type": "string",
                        "value": "異常回報",
                        "format": "n/a",
                        "id": "buttonName"
                    },
                    "buttonId": {
                        "name": "按鈕ID",
                        "type": "string",
                        "value": "responeIrregular",
                        "format": "n/a",
                        "id": "buttonId"
                    }
                }
               ],
               "format":"n/a",
               "id":"buttonList"
            }
         },
         "format":"n/a",
         "id":"editableButton"
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
