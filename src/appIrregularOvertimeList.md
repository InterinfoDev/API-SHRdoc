# appIrregularOvertimeList
取得加班異常列表資訊

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
| request | {empid:admin,cpnyid:TW,yymm:202207,skind:A,before:30,after:30,uncard:30} | Object | 查詢條件(depNumber/empid至少選一輸入)

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin", 
        "cpnyid":"TW",
        "yymm":"202207",
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
| yymm | 202207 | Array(Integer) | 查詢年月 | Y | AC(YYYYmm) |
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
        "YYYYmm": {
          "name": "加班異常年月",
          "type": "string",
          "value": "202207",
          "format": "YYYYmm",
          "id": "YYYYmm"
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
            "overtimeState": {
              "name": "加班情況",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "overtimeState"
            },
            "inCard": {
              "name": "進卡",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "inCard"
            },
            "empid": {
              "name": "員工編號",
              "type": "string",
              "value": "admin",
              "format": "n/a",
              "id": "empid"
            },
            "errorReason": {
              "name": "異常說明",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorReason"
            },
            "class": {
              "name": "班別",
              "type": "string",
              "value": "早班(8-17)",
              "format": "n/a",
              "id": "class"
            },
            "notApprovedAddOvertime": {
              "name": "未簽核加班單",
              "type": "string",
              "value": "加班1800-2100=3.00小時",
              "format": "n/a",
              "id": "noSignoffAddovertime"
            },
            "classEndTime": {
              "name": "班別時間(迄)",
              "type": "string",
              "value": "1700",
              "format": "HHmm",
              "id": "classEndTime"
            },
            "classStarTime": {
              "name": "班別時間(起)",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "classStarTime"
            },
            "errorRespone": {
              "name": "異常回應",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorRespone"
            },
            "outCard": {
              "name": "出卡",
              "type": "string",
              "value": "1700",
              "format": "HHmm",
              "id": "outCard"
            },
            "empFullName": {
              "name": "員工姓名",
              "type": "string",
              "value": "系統管理員",
              "format": "n/a",
              "id": "empFullName"
            },
            "depFullName": {
              "name": "部門名稱",
              "type": "string",
              "value": "99999 英特內股份有限公司",
              "format": "n/a",
              "id": "depFullName"
            },
            "dayofweek": {
              "name": "異常日期星期",
              "type": "integer",
              "value": 1,
              "format": "dayofweek",
              "id": "dayofweek"
            },
            "errorDate": {
              "name": "異常日期",
              "type": "string",
              "value": "20220704",
              "format": "YYYYmmdd",
              "id": "errorDate"
            }
          },
          "format": "n/a",
          "id": "IrregularOvertimeInformation"
        },
        {
          "name": "員工加班異常資訊",
          "type": "object",
          "value": {
            "overtimeState": {
              "name": "加班情況",
              "type": "string",
              "value": "加班給薪4.0小時",
              "format": "n/a",
              "id": "overtimeState"
            },
            "inCard": {
              "name": "進卡",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "inCard"
            },
            "empid": {
              "name": "員工編號",
              "type": "string",
              "value": "admin",
              "format": "n/a",
              "id": "empid"
            },
            "errorReason": {
              "name": "異常說明",
              "type": "string",
              "value": "刷卡時間 0800 2406,申請加班1700-1900=2.00,申請加班1700-1900=2.00,超過%1分鐘,異常原因,加班時數不足",
              "format": "n/a",
              "id": "errorReason"
            },
            "class": {
              "name": "班別",
              "type": "string",
              "value": "早班(8-17)",
              "format": "n/a",
              "id": "class"
            },
            "notApprovedAddOvertime": {
              "name": "未簽核加班單",
              "type": "string",
              "value": "加班1700-1900=2.00小時 加班1700-1900=2.00小時",
              "format": "n/a",
              "id": "noSignoffAddovertime"
            },
            "classEndTime": {
              "name": "班別時間(迄)",
              "type": "string",
              "value": "1700",
              "format": "HHmm",
              "id": "classEndTime"
            },
            "classStarTime": {
              "name": "班別時間(起)",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "classStarTime"
            },
            "errorRespone": {
              "name": "異常回應",
              "type": "string",
              "value": "測試",
              "format": "n/a",
              "id": "errorRespone"
            },
            "outCard": {
              "name": "出卡",
              "type": "string",
              "value": "0006",
              "format": "HHmm",
              "id": "outCard"
            },
            "empFullName": {
              "name": "員工姓名",
              "type": "string",
              "value": "系統管理員",
              "format": "n/a",
              "id": "empFullName"
            },
            "depFullName": {
              "name": "部門名稱",
              "type": "string",
              "value": "99999 英特內股份有限公司",
              "format": "n/a",
              "id": "depFullName"
            },
            "dayofweek": {
              "name": "異常日期星期",
              "type": "integer",
              "value": 2,
              "format": "dayofweek",
              "id": "dayofweek"
            },
            "errorDate": {
              "name": "異常日期",
              "type": "string",
              "value": "20220705",
              "format": "YYYYmmdd",
              "id": "errorDate"
            }
          },
          "format": "n/a",
          "id": "travel"
        },
        {
          "name": "員工加班異常資訊",
          "type": "object",
          "value": {
            "overtimeState": {
              "name": "加班情況",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "overtimeState"
            },
            "inCard": {
              "name": "進卡",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "inCard"
            },
            "empid": {
              "name": "員工編號",
              "type": "string",
              "value": "admin",
              "format": "n/a",
              "id": "empid"
            },
            "errorReason": {
              "name": "異常說明",
              "type": "string",
              "value": "刷卡時間 0800 2225,異常原因,刷卡時間往後%1分鐘,未報加班",
              "format": "n/a",
              "id": "errorReason"
            },
            "class": {
              "name": "班別",
              "type": "string",
              "value": "早班(8-17)",
              "format": "n/a",
              "id": "class"
            },
            "notApprovedAddOvertime": {
              "name": "未簽核加班單",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "noSignoffAddovertime"
            },
            "classEndTime": {
              "name": "班別時間(迄)",
              "type": "string",
              "value": "1700",
              "format": "HHmm",
              "id": "classEndTime"
            },
            "classStarTime": {
              "name": "班別時間(起)",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "classStarTime"
            },
            "errorRespone": {
              "name": "異常回應",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorRespone"
            },
            "outCard": {
              "name": "出卡",
              "type": "string",
              "value": "2225",
              "format": "HHmm",
              "id": "outCard"
            },
            "empFullName": {
              "name": "員工姓名",
              "type": "string",
              "value": "系統管理員",
              "format": "n/a",
              "id": "empFullName"
            },
            "depFullName": {
              "name": "部門名稱",
              "type": "string",
              "value": "99999 英特內股份有限公司",
              "format": "n/a",
              "id": "depFullName"
            },
            "dayofweek": {
              "name": "異常日期星期",
              "type": "integer",
              "value": 3,
              "format": "dayofweek",
              "id": "dayofweek"
            },
            "errorDate": {
              "name": "異常日期",
              "type": "string",
              "value": "20220706",
              "format": "YYYYmmdd",
              "id": "errorDate"
            }
          },
          "format": "n/a",
          "id": "travel"
        },
        {
          "name": "員工加班異常資訊",
          "type": "object",
          "value": {
            "overtimeState": {
              "name": "加班情況",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "overtimeState"
            },
            "inCard": {
              "name": "進卡",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "inCard"
            },
            "empid": {
              "name": "員工編號",
              "type": "string",
              "value": "admin",
              "format": "n/a",
              "id": "empid"
            },
            "errorReason": {
              "name": "異常說明",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorReason"
            },
            "class": {
              "name": "班別",
              "type": "string",
              "value": "早班(8-17)",
              "format": "n/a",
              "id": "class"
            },
            "notApprovedAddOvertime": {
              "name": "未簽核加班單",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "noSignoffAddovertime"
            },
            "classEndTime": {
              "name": "班別時間(迄)",
              "type": "string",
              "value": "1700",
              "format": "HHmm",
              "id": "classEndTime"
            },
            "classStarTime": {
              "name": "班別時間(起)",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "classStarTime"
            },
            "errorRespone": {
              "name": "異常回應",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorRespone"
            },
            "outCard": {
              "name": "出卡",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "outCard"
            },
            "empFullName": {
              "name": "員工姓名",
              "type": "string",
              "value": "系統管理員",
              "format": "n/a",
              "id": "empFullName"
            },
            "depFullName": {
              "name": "部門名稱",
              "type": "string",
              "value": "99999 英特內股份有限公司",
              "format": "n/a",
              "id": "depFullName"
            },
            "dayofweek": {
              "name": "異常日期星期",
              "type": "integer",
              "value": 2,
              "format": "dayofweek",
              "id": "dayofweek"
            },
            "errorDate": {
              "name": "異常日期",
              "type": "string",
              "value": "20220719",
              "format": "YYYYmmdd",
              "id": "errorDate"
            }
          },
          "format": "n/a",
          "id": "travel"
        },
        {
          "name": "員工加班異常資訊",
          "type": "object",
          "value": {
            "overtimeState": {
              "name": "加班情況",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "overtimeState"
            },
            "inCard": {
              "name": "進卡",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "inCard"
            },
            "empid": {
              "name": "員工編號",
              "type": "string",
              "value": "admin",
              "format": "n/a",
              "id": "empid"
            },
            "errorReason": {
              "name": "異常說明",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorReason"
            },
            "class": {
              "name": "班別",
              "type": "string",
              "value": "早班(8-17)",
              "format": "n/a",
              "id": "class"
            },
            "notApprovedAddOvertime": {
              "name": "未簽核加班單",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "noSignoffAddovertime"
            },
            "classEndTime": {
              "name": "班別時間(迄)",
              "type": "string",
              "value": "1700",
              "format": "HHmm",
              "id": "classEndTime"
            },
            "classStarTime": {
              "name": "班別時間(起)",
              "type": "string",
              "value": "0800",
              "format": "HHmm",
              "id": "classStarTime"
            },
            "errorRespone": {
              "name": "異常回應",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorRespone"
            },
            "outCard": {
              "name": "出卡",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "outCard"
            },
            "empFullName": {
              "name": "員工姓名",
              "type": "string",
              "value": "系統管理員",
              "format": "n/a",
              "id": "empFullName"
            },
            "depFullName": {
              "name": "部門名稱",
              "type": "string",
              "value": "99999 英特內股份有限公司",
              "format": "n/a",
              "id": "depFullName"
            },
            "dayofweek": {
              "name": "異常日期星期",
              "type": "integer",
              "value": 3,
              "format": "dayofweek",
              "id": "dayofweek"
            },
            "errorDate": {
              "name": "異常日期",
              "type": "string",
              "value": "20220720",
              "format": "YYYYmmdd",
              "id": "errorDate"
            }
          },
          "format": "n/a",
          "id": "travel"
        },
        {
          "name": "員工加班異常資訊",
          "type": "object",
          "value": {
            "overtimeState": {
              "name": "加班情況",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "overtimeState"
            },
            "inCard": {
              "name": "進卡",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "inCard"
            },
            "empid": {
              "name": "員工編號",
              "type": "string",
              "value": "admin",
              "format": "n/a",
              "id": "empid"
            },
            "errorReason": {
              "name": "異常說明",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorReason"
            },
            "class": {
              "name": "班別",
              "type": "string",
              "value": "例假日",
              "format": "n/a",
              "id": "class"
            },
            "notApprovedAddOvertime": {
              "name": "未簽核加班單",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "noSignoffAddovertime"
            },
            "classEndTime": {
              "name": "班別時間(迄)",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "classEndTime"
            },
            "classStarTime": {
              "name": "班別時間(起)",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "classStarTime"
            },
            "errorRespone": {
              "name": "異常回應",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "errorRespone"
            },
            "outCard": {
              "name": "出卡",
              "type": "string",
              "value": "",
              "format": "HHmm",
              "id": "outCard"
            },
            "empFullName": {
              "name": "員工姓名",
              "type": "string",
              "value": "系統管理員",
              "format": "n/a",
              "id": "empFullName"
            },
            "depFullName": {
              "name": "部門名稱",
              "type": "string",
              "value": "99999 英特內股份有限公司",
              "format": "n/a",
              "id": "depFullName"
            },
            "dayofweek": {
              "name": "異常日期星期",
              "type": "integer",
              "value": 6,
              "format": "dayofweek",
              "id": "dayofweek"
            },
            "errorDate": {
              "name": "異常日期",
              "type": "string",
              "value": "20220730",
              "format": "YYYYmmdd",
              "id": "errorDate"
            }
          },
          "format": "n/a",
          "id": "travel"
        },
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
          "value": "系統管理員",
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
          "value": "Administrator",
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
