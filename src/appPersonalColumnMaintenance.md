# appPersonalColumnMaintenance
個人資料維護欄位

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPersonalColumnMaintenance
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### fieldType
| Type | Description |
|:---------|:------------|
| input | 文字輸入類型 |
| select | 單選類型 |
| alternative | 多選類型 |
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
      "isFlow":{
         "name":"是否有簽核單據",
         "type":"boolean",
         "value":true,
         "format":"n/a",
         "id":"isFlow"
      },
      "isFlowMessage": {
         "name": "有簽核單據顯示訊息",
         "type": "string",
         "value": "您的資料正在覆核中，請待覆核完成後再修改",
         "format": "n/a",
         "id": "isFlowMessage"
      },
      "employee":{
         "name":"個人資料維護欄位",
         "type":"array",
         "value":[
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"input",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldKey":{
                     "name":"欄位序號",
                     "type":"string",
                     "value":"108418179393993612479",
                     "format":"n/a",
                     "id":"fieldKey"
                  },
                  "visiable":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"visiable"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"empid",
                     "format":"n/a",
                     "id":"fieldId"
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
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0105"
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
               "id":"empid"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"input",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldKey":{
                     "name":"欄位序號",
                     "type":"string",
                     "value":"101790650935424122480",
                     "format":"n/a",
                     "id":"fieldKey"
                  },
                  "visiable":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"visiable"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"empFullName",
                     "format":"n/a",
                     "id":"fieldId"
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
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "郁O如"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"中文姓名",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"empFullName"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"select",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldKey":{
                     "name":"欄位序號",
                     "type":"string",
                     "value":"101396267003611582294",
                     "format":"n/a",
                     "id":"fieldKey"
                  },
                  "visiable":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"visiable"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"schoolType",
                     "format":"n/a",
                     "id":"fieldId"
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
                        {
                           "optionId":{
                              "name":"選單代號",
                              "type":"string",
                              "value":"A",
                              "format":"n/a",
                              "id":"optionId"
                           },
                           "optionValue":{
                              "name":"選單名稱",
                              "type":"string",
                              "value":"日間部",
                              "format":"n/a",
                              "id":"optionValue"
                           }
                        },
                        {
                           "optionId":{
                              "name":"選單代號",
                              "type":"string",
                              "value":"B",
                              "format":"n/a",
                              "id":"optionId"
                           },
                           "optionValue":{
                              "name":"選單名稱",
                              "type":"string",
                              "value":"夜間部",
                              "format":"n/a",
                              "id":"optionValue"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"option"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "A"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"日夜間部",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"schoolType"
            }
         ],
         "format":"n/a",
         "id":"employee"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "YYYYmm":"西元年月"
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
