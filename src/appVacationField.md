# appVacationField
請假單申請畫面欄位

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationField
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
| request | {specialDate:XXX, empid:admin, vacationCode:XXX} | Object | 查詢條件(依據申請畫面取得)

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "specialDate":"0220425", 
        "empid":"admin",
        "vacationCode":"06.061"
    }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| specialDate | 20220425 | String | 特殊日期 | N | AC(YYYYmmdd) |
| empid | admin | String | 員工編號 | Y | n/a |
| vacationCode | admin | String | 價別代碼 | Y | n/a |

### fieldType
| Type | Description |
|:---------|:------------|
| input | 文字輸入類型 |
| select | 單選類型 |
| switch | 開關類型 |
| upload | 檔案上傳類型 |
| dateYMD | 日期類型(年月日) |
| dateYM | 日期類型(年月) |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "employee":{
         "name":"申請者基本資料",
         "type":"object",
         "value":{
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系O管",
               "format":"n/a",
               "id":"empFullName"
            },
            "vacationName":{
               "name":"假別名稱",
               "type":"string",
               "value":"喪假",
               "format":"n/a",
               "id":"vacationName"
            },
            "depFullName":{
               "name":"部門名稱",
               "type":"string",
               "value":"L1線B班",
               "format":"n/a",
               "id":"depFullName"
            },
            "vacationCode":{
               "name":"假別代碼",
               "type":"string",
               "value":"06.061",
               "format":"n/a",
               "id":"vacationCode"
            },
            "companyId":{
               "name":"公司代號",
               "type":"string",
               "value":"TW",
               "format":"n/a",
               "id":"companyId"
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
               "value":"14122",
               "format":"n/a",
               "id":"depCode"
            },
            "companyFullName":{
               "name":"公司全名",
               "type":"string",
               "value":"72英特內全名(中和)",
               "format":"n/a",
               "id":"companyFullName"
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
            "ticket":"張"
         }
      },
      "vacationField":{
         "name":"請假單欄位資訊",
         "type":"array",
         "value":[
            {
               "name":"前置假",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"input",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"preVacationCode",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "visiable":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"visiable"
                  },
                  "editable":{
                     "name":"開放編輯",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"editable"
                  },
                  "option":{
                     "name":"選單項目",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"option"
                  },
                  "note":{
                     "name":"欄位備註",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"note"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"前置假",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"preVacationCode"
            },
            {
               "name":"特別日期",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"dateYMD",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"specDate",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "visiable":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"visiable"
                  },
                  "editable":{
                     "name":"開放編輯",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"editable"
                  },
                  "option":{
                     "name":"選單項目",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"option"
                  },
                  "note":{
                     "name":"欄位備註",
                     "type":"string",
                     "value":"喪假：往生日期",
                     "format":"n/a",
                     "id":"note"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"string",
                     "value":"20220425",
                     "format":"YYYYmmdd",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"特別日期",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"specDate"
            },
            {
               "name":"延遲請假原因",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"input",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"delayNote",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "visiable":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"visiable"
                  },
                  "editable":{
                     "name":"開放編輯",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"editable"
                  },
                  "option":{
                     "name":"選單項目",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"option"
                  },
                  "note":{
                     "name":"欄位備註",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"note"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"延遲請假原因",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"delayNote"
            }
         ],
         "format":"n/a",
         "id":"vacationField"
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
