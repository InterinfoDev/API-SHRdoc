# appIrregularOvertimeList
取得加班異常列表資訊

(回傳值 星期都會以數字格式 ex:0(星期日、1(星期一)...))
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
| request | {empid:admin,cpnyid:TW,irragularYM:202207,skind:A,before:30,after:30,uncard:30} | Object |

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
        "skind":"A",
        "before":30,
        "after":30,
        "uncard":30
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
| cpnyid | TW | String | 公司代號 | Y | n/a |
| irragularYM | 202207 | String | 查詢年月 | Y | AC(YYYYmm) |
| skind | A | String | 顯示種類 | Y | n/a |
| before | 30 | Integer | 提前多久刷卡視為異常 | Y | n/a |
| after | 30 | Integer | 延後多久刷卡視為異常 | Y | n/a |
| uncard | 30 | Integer | 刷卡時間超過多久未報加班視為異常 | Y | n/a |


### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "main": {
            "name": "加班異常資訊",
            "type": "object",
            "value": {
                "irragularYM": {            --  richard 修改名稱 irragularYM
                    "name": "加班異常年月",
                    "type": "string",
                    "value": "202207",
                    "format": "irragularYM",
                    "id": "irragularYM"     --  richard 修改名稱 irragularYM
                }
            },
            "format": "n/a",
            "id": "main"
        },
        "appIrregularOvertimeList": {
            "name": "員工加班異常列表",
            "type": "array",
            "value": [
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220701",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "workClassName": {                     --richard 修改欄位名稱
                                    "name": "班別",
                                    "type": "string",
                                    "value": "0常日班8h：0830-1730",
                                    "format": "n/a",
                                    "id": "workClassName"              --richard 修改欄位名稱
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 5,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 5,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStartTime": {         --richard 修改欄位名稱 classStartTime
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "classStartTime"   --richard 修改欄位名稱 classStartTime
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "1730",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220701",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220702",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "green",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "休息日",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "green",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 6,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 6,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220702",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220703",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "例假日",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 0,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 0,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220703",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220708",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "0常日班8h：0830-1730",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 5,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 5,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "1730",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220708",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220712",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "0常日班8h：0830-1730",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 2,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 2,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "1730",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220712",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220713",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "0常日班8h：0830-1730",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 3,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 3,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "1730",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220713",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220714",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "0常日班8h：0830-1730",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "black",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 4,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 4,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "0830",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "1730",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220714",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                },
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "detailInfor": {
                            "name": "展開資料",
                            "type": "object",
                            "value": {
                                "inCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "inCard"
                                },
                                "errorRespone": {
                                    "name": "異常回應",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorRespone"
                                },
                                "overtimeState": {
                                    "name": "加班情況",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "overtimeState"
                                },
                                "classColor": {
                                    "name": "班別顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "classColor"
                                },
                                "outCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "outCard"
                                },
                                "empid": {
                                    "name": "員工編號",
                                    "type": "string",
                                    "value": "admin",
                                    "format": "n/a",
                                    "id": "empid"
                                },
                                "errorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220731",
                                    "format": "YYYYmmdd",
                                    "id": "errorDate"
                                },
                                "simpleDayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "simpleDayOfWeekColor"
                                },
                                "class": {
                                    "name": "班別",
                                    "type": "string",
                                    "value": "例假日",
                                    "format": "n/a",
                                    "id": "class"
                                },
                                "unApproved": {
                                    "name": "未簽核加班單",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "unApproved"
                                },
                                "dayOfWeekColor": {
                                    "name": "異常日期顏色",
                                    "type": "string",
                                    "value": "red",
                                    "format": "n/a",
                                    "id": "dayOfWeekColor"
                                },
                                "dayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 0,
                                    "format": "dayofweek",
                                    "id": "dayOfWeek"
                                },
                                "errorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "errorReason"
                                },
                                "simpleDayOfWeek": {
                                    "name": "異常日期星期",
                                    "type": "integer",
                                    "value": 0,
                                    "format": "dayofweek",
                                    "id": "simpleDayOfWeek"
                                },
                                "classStarTime": {
                                    "name": "班別時間(起)",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "classStarTime"
                                },
                                "empFullName": {
                                    "name": "員工姓名",
                                    "type": "string",
                                    "value": "管理者",
                                    "format": "n/a",
                                    "id": "empFullName"
                                },
                                "depFullName": {
                                    "name": "部門名稱",
                                    "type": "string",
                                    "value": "A 中保集團",
                                    "format": "n/a",
                                    "id": "depFullName"
                                },
                                "classEndTime": {
                                    "name": "班別時間(迄)",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "classEndTime"
                                }
                            },
                            "format": "n/a",
                            "id": "detailInfor"
                        },
                        "simpleInfor": {
                            "name": "簡易資料",
                            "type": "object",
                            "value": {
                                "simpleErrorDate": {
                                    "name": "異常日期",
                                    "type": "string",
                                    "value": "20220731",
                                    "format": "YYYYmmdd",
                                    "id": "simpleErrorDate"
                                },
                                "simpleErrorReason": {
                                    "name": "異常說明",
                                    "type": "string",
                                    "value": "",
                                    "format": "n/a",
                                    "id": "simpleErrorReason"
                                },
                                "simpleInCard": {
                                    "name": "進卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleInCard"
                                },
                                "simpleOutCard": {
                                    "name": "出卡",
                                    "type": "string",
                                    "value": "",
                                    "format": "HHmm",
                                    "id": "simpleOutCard"
                                }
                            },
                            "format": "n/a",
                            "id": "simpleInfor"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                }
            ],
            "format": "n/a",
            "id": "appIrregularOvertimeList"
        },
        "employee": {
            "name": "員工基本資料",
            "type": "object",
            "value": {
                "empFullName": {
                    "name": "員工中文姓名",
                    "type": "string",
                    "value": "管理者",
                    "format": "n/a",
                    "id": "empFullName"
                },
                "empid": {
                    "name": "員工編號",
                    "type": "string",
                    "value": "admin",
                    "format": "n/a",
                    "id": "empid"
                },
                "empFullEname": {
                    "name": "員工英文姓名",
                    "type": "string",
                    "value": "",
                    "format": "n/a",
                    "id": "empFullEname"
                }
            },
            "format": "n/a",
            "id": "employee"
        },
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "YYYYmmdd": "西元年月日",
                "n/a": "",
                "dayofweek": "星期"
            }
        },
        "editableButton": {
            "name": "可使用功能按鈕資訊",
            "type": "object",
            "value": {
                "buttonList": {
                    "name": "按鈕清單",
                    "type": "object",
                    "value": [
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
                    "format": "n/a",
                    "id": "buttonList"
                }
            },
            "format": "n/a",
            "id": "editableButton"
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
