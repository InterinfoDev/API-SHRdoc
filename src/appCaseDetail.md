# appCaseDetail
未結案詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appCaseDetail
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {key:xxx} | Object | 查詢條件 |


### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "key":"635144642219404571194688689683105522531368129784502001284860188282814076207411"
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
| key | 635144642219404571194688689683105522531368129784502001284860188282814076207411 | String | 鍵值 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "detailList":{
         "name":"未結案清單",
         "type":"array",
         "value":[
            {
               "name":"清單資訊",
               "type":"object",
               "value":{
                  "fieldList":{
                     "name":"欄位清單",
                     "type":"array",
                     "value":[
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"承辦者回覆 1617 楊O齊",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"待簽資料",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"14122 L1線B班",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"單位",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"admin",
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
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"系O管",
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
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20191106",
                              "format":"YYYYmmdd",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"需求日期",
                              "format":"YYYYmmdd",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20191105",
                              "format":"YYYYmmdd",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請日期",
                              "format":"YYYYmmdd",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"095513",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請時間",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"fieldList"
                  }
               },
               "format":"n/a",
               "id":"detail"
            },
            {
               "name":"清單資訊",
               "type":"object",
               "value":{
                  "fieldList":{
                     "name":"欄位清單",
                     "type":"array",
                     "value":[
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"承辦者回覆 admin 系O管",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"待簽資料",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"14122 L1線B班",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"單位",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"admin",
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
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"系O管",
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
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20191108",
                              "format":"YYYYmmdd",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"需求日期",
                              "format":"YYYYmmdd",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20191105",
                              "format":"YYYYmmdd",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請日期",
                              "format":"YYYYmmdd",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"100138",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請時間",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"fieldList"
                  }
               },
               "format":"n/a",
               "id":"detail"
            }
         ],
         "format":"n/a",
         "id":"detailList"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "YYYY":"西元年",
            "n/a":"",
            "YYYYmm":"西元年月"
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有Personal資料，若Personal無資料，則出錯。
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
