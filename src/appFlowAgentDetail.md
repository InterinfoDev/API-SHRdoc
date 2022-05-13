# appFlowAgentDetail
查詢單筆簽核代理人詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowAgentDetail
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
| request | {'cpnyid':'TW' ,'empid':'admin' ,'func_name':'C.126.個人工作目標修改簽核' ,'dept_no':'89' ,'agent':'110000311'} | Object | 查詢條件(依據使用者所選擇要查看的公司、員工、代理功能、部門、簽核代理人，取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cpnyid":"TW", 
        "empid":"admin", 
        "func_name":"C.126.個人工作目標修改簽核",
        "dept_no":"89",
        "agent":"110000311"
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
| cpnyid | 202201 | String | 公司別 | Y | n/a |
| empid | admin | String | 員工編號 | Y | n/a |
| func_name | 00 | String | 代理功能 | Y | n/a |
| dept_no | admin | int | 部門 | Y | n/a |
| agent | 00 | String | 簽核代理人 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "deleteFlowAgent":{
         "name":"刪除簽核代理人",
         "type":"object",
         "value":{
            "deleteKey":{
               "name":"刪除鍵值",
               "type":"string",
               "value":"4326084225293747024556419988109226030786170329214256400024434116838672769187526122578773346158145806659984556753490868565199631711318172",
               "format":"n/a",
               "id":"deleteKey"
            }
         },
         "format":"n/a",
         "id":"deleteFlowAgent"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "day":"天",
            "n/a":""
         }
      },
      "flowAgentDetail":{
         "name":"簽核代理人詳細資訊",
         "type":"object",
         "value":[
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"empid",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "admin"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"員工編號",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"empFullName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "系統管理員"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"員工姓名",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"function",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "C.126.個人工作目標修改簽核"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"代理功能",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"agent",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "110000311"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"簽核代理人編號",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"agentName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "解O庭"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"簽核代理人姓名",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"startTime",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "2021/09/01 00:00"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"代理起始時間",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"endTime",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "2021/09/01 23:59"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"代理結束時間",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            }
         ],
         "format":"n/a",
         "id":"flowAgentDetail"
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
