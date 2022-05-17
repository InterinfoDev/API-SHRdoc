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
                     "value":"員工中文姓名",
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
                     "value":"empFullEname",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "Administrator"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"員工英文姓名",
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
                     "value":"depCode",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "14122"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"部門代號",
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
                     "value":"depFullName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "L1線B班"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"部門名稱",
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
                     "value":"cardDate",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "20210601"
                     ],
                     "format":"YYYYmmdd",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"補卡日期",
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
                     "value":"cardTime",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0600"
                     ],
                     "format":"HHmm",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"補卡時間",
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
                     "value":"cardType",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "其他"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"進出別",
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
                     "value":"addDate",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "20210629"
                     ],
                     "format":"YYYYmmdd",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"申請日期",
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
                     "value":"reason",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "忘刷卡"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"補登原因",
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
                     "value":"note",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "test"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"備註",
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
                     "value":"approvalStatus",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "未生效"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"簽核狀態",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
                "name": "欄位資訊",
                "type": "object",
                "value": {
                    "fieldType": {
                        "name": "欄位類型",
                        "type": "string",
                        "value": "file",
                        "format": "n/a",
                        "id": "fieldType"
                    },
                    "fieldId": {
                        "name": "欄位代號",
                        "type": "string",
                        "value": "uploadFiles",
                        "format": "n/a",
                        "id": "fieldId"
                    },
                    "files": {
                        "name": "附件資訊",
                        "type": "array",
                        "value": [
                            {
                                "fileType": {
                                    "name": "檔案類型",
                                    "type": "string",
                                    "value": "image/jpeg",
                                    "format": "n/a",
                                    "id": "fileType"
                                },
                                "fileUrl": {
                                    "name": "檔案路徑",
                                    "type": "string",
                                    "value": "72498637980750425429295356143326706787584885528416948278334572143182089604433418700793583203058856941247560633788884871878908572476551182063374002250063452",
                                    "format": "n/a",
                                    "id": "fileUrl"
                                },
                                "fileName": {
                                    "name": "檔案名稱",
                                    "type": "string",
                                    "value": "1652778534169_1652056356494.jpg",
                                    "format": "n/a",
                                    "id": "fileName"
                                }
                            }
                        ],
                        "format": "n/a",
                        "id": "files"
                    },
                    "fieldName": {
                        "name": "欄位名稱",
                        "type": "string",
                        "value": "附件",
                        "format": "n/a",
                        "id": "fieldName"
                    }
                },
                "format": "n/a",
                "id": "field"
            },
         ],
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
