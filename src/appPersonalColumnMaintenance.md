# appPersonalColumnMaintenance
個人資料維護欄位

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPersonalColumnMaintenance
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
      "properties":{
         "format":{
            "YYYYmm":"西元年月",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "employee":{
         "id":"employee",
         "name":"個人資料維護欄位",
         "value":[
            {
               "id":"108617422147702250851",
               "name":"欄位資訊",
               "value":{
                  "fieldId":{
                     "id":"108617422147702250851",
                     "name":"欄位代號",
                     "value":"photo",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldName":{
                     "id":"fieldName",
                     "name":"欄位名稱",
                     "value":"員工照片",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldType":{
                     "id":"fieldType",
                     "name":"欄位類型",
                     "value":"upload",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldValue":{
                     "id":"fieldValue",
                     "name":"欄位資料",
                     "value":[
                        ""
                     ],
                     "type":"array",
                     "format":"base64"
                  },
                  "editable":{
                     "id":"editable",
                     "name":"開放編輯",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "visiable":{
                     "id":"visiable",
                     "name":"是否顯示",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "option":{
                     "id":"option",
                     "name":"選單項目",
                     "value":[
                        
                     ],
                     "type":"array",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"108617422147704250851",
               "name":"欄位資訊",
               "value":{
                  "fieldId":{
                     "id":"fieldId",
                     "name":"欄位代號",
                     "value":"108617422147704250851",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldName":{
                     "id":"fieldName",
                     "name":"欄位名稱",
                     "value":"員工中文姓名",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldType":{
                     "id":"fieldType",
                     "name":"欄位類型",
                     "value":"input",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldValue":{
                     "id":"fieldValue",
                     "name":"欄位資料",
                     "value":[
                        "林奇杰"
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "editable":{
                     "id":"editable",
                     "name":"開放編輯",
                     "value":false,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "visiable":{
                     "id":"visiable",
                     "name":"是否顯示",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "option":{
                     "id":"option",
                     "name":"選單項目",
                     "value":[
                        
                     ],
                     "type":"array",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"108617422147704250423",
               "name":"欄位資訊",
               "value":{
                  "fieldId":{
                     "id":"fieldId",
                     "name":"欄位代號",
                     "value":"108617422147704250423",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldName":{
                     "id":"fieldName",
                     "name":"欄位名稱",
                     "value":"員工英文姓名",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldType":{
                     "id":"fieldType",
                     "name":"欄位類型",
                     "value":"input",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldValue":{
                     "id":"fieldValue",
                     "name":"欄位資料",
                     "value":[
                        "Lucas"
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "editable":{
                     "id":"editable",
                     "name":"開放編輯",
                     "value":false,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "visiable":{
                     "id":"visiable",
                     "name":"是否顯示",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "option":{
                     "id":"option",
                     "name":"選單項目",
                     "value":[
                        
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "type":"object",
                  "format":"n/a"
               }
            },
            {
               "id":"108617422147704250533",
               "name":"欄位資訊",
               "value":{
                  "fieldId":{
                     "id":"fieldId",
                     "name":"欄位代號",
                     "value":"108617422147704250533",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldName":{
                     "id":"fieldName",
                     "name":"欄位名稱",
                     "value":"工作地點",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldType":{
                     "id":"fieldType",
                     "name":"欄位類型",
                     "value":"select",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldValue":{
                     "id":"fieldValue",
                     "name":"欄位資料",
                     "value":[
                        "A1"
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "editable":{
                     "id":"editable",
                     "name":"開放編輯",
                     "value":false,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "visiable":{
                     "id":"visiable",
                     "name":"是否顯示",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "option":{
                     "id":"option",
                     "name":"選單項目",
                     "value":[
                        {
                           "optionId":{
                              "id":"optionId",
                              "name":"選單代號",
                              "value":"A",
                              "type":"string",
                              "format":"n/a"
                           },
                           "optionValue":{
                              "id":"optionValue",
                              "name":"選單名稱",
                              "value":"台北",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "optionId":{
                              "id":"optionId",
                              "name":"選單代號",
                              "value":"B",
                              "type":"string",
                              "format":"n/a"
                           },
                           "optionValue":{
                              "id":"optionValue",
                              "name":"選單名稱",
                              "value":"新竹",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "optionId":{
                              "id":"optionId",
                              "name":"選單代號",
                              "value":"C",
                              "type":"string",
                              "format":"n/a"
                           },
                           "optionValue":{
                              "id":"optionValue",
                              "name":"選單名稱",
                              "value":"高雄",
                              "type":"string",
                              "format":"n/a"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"10861742214770423332",
               "name":"欄位資訊",
               "value":{
                  "fieldId":{
                     "id":"fieldId",
                     "name":"欄位代號",
                     "value":"10861742214770423332",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldName":{
                     "id":"fieldName",
                     "name":"欄位名稱",
                     "value":"性別",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldType":{
                     "id":"fieldType",
                     "name":"欄位類型",
                     "value":"select",
                     "type":"string",
                     "format":"n/a"
                  },
                  "fieldValue":{
                     "id":"fieldValue",
                     "name":"欄位資料",
                     "value":[
                        "M"
                     ],
                     "type":"array",
                     "format":"n/a"
                  },
                  "editable":{
                     "id":"editable",
                     "name":"開放編輯",
                     "value":false,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "visiable":{
                     "id":"visiable",
                     "name":"是否顯示",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "option":{
                     "id":"option",
                     "name":"選單項目",
                     "value":[
                        {
                           "optionId":{
                              "id":"optionId",
                              "name":"選單代號",
                              "value":"M",
                              "type":"string",
                              "format":"n/a"
                           },
                           "optionValue":{
                              "id":"optionValue",
                              "name":"選單名稱",
                              "value":"男性",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "optionId":{
                              "id":"optionId",
                              "name":"選單代號",
                              "value":"F",
                              "type":"string",
                              "format":"n/a"
                           },
                           "optionValue":{
                              "id":"optionValue",
                              "name":"選單名稱",
                              "value":"女性",
                              "type":"string",
                              "format":"n/a"
                           }
                        }
                     ],
                     "type":"array",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
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
