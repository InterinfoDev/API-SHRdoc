# appFlowList
取得使用者待簽核單據詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowList
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
| request | {functionName:xxx,flowState:xxx} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "functionName":"CA4.行政服務單簽核",
        "flowState":"簽核群組第1階",
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
| functionName | CA4.行政服務單簽核 | String | 簽核單據名稱 | Y | n/a |
| flowState | 簽核群組第1階 | String | 簽核節點名稱 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "HRFlowList":{
         "id":"HRFlowList",
         "name":"CA4.行政服務單簽核-待簽核列表",
         "value":[
            {
               "id":"0",
               "name":"No.1",
               "value":{
                  "fields":{
                     "name":"欄位資訊",
                     "type":"array",
                     "value":[
                        {
                           "fieldValue":{
                              "id":"fieldValue",
                              "name":"欄位資料",
                              "value":"14121 L1線A班",
                              "type":"string",
                              "format":"n/a"
                           },
                           "fieldName":{
                              "id":"fieldName",
                              "name":"欄位名稱",
                              "value":"單位",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "fieldValue":{
                              "id":"fieldValue",
                              "name":"欄位資料",
                              "value":"admin",
                              "type":"string",
                              "format":"n/a"
                           },
                           "fieldName":{
                              "id":"fieldName",
                              "name":"欄位名稱",
                              "value":"員工編號",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "fieldValue":{
                              "id":"fieldValue",
                              "name":"欄位資料",
                              "value":"系O管",
                              "type":"string",
                              "format":"n/a"
                           },
                           "fieldName":{
                              "id":"fieldName",
                              "name":"欄位名稱",
                              "value":"員工姓名",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "fieldValue":{
                              "id":"fieldValue",
                              "name":"欄位資料",
                              "value":"20200520",
                              "type":"string",
                              "format":"n/a"
                           },
                           "fieldName":{
                              "id":"fieldName",
                              "name":"欄位名稱",
                              "value":"需求日期",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "fieldValue":{
                              "id":"fieldValue",
                              "name":"欄位資料",
                              "value":"20200515",
                              "type":"string",
                              "format":"n/a"
                           },
                           "fieldName":{
                              "id":"fieldName",
                              "name":"欄位名稱",
                              "value":"申請日期",
                              "type":"string",
                              "format":"n/a"
                           }
                        },
                        {
                           "fieldValue":{
                              "id":"fieldValue",
                              "name":"欄位資料",
                              "value":"102500",
                              "type":"string",
                              "format":"n/a"
                           },
                           "fieldName":{
                              "id":"fieldName",
                              "name":"欄位名稱",
                              "value":"申請時間",
                              "type":"string",
                              "format":"n/a"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"fields"
                  },
                  "keys":{
                     "name":"欄位鍵值",
                     "type":"array",
                     "value":[
                        {
                           "uniqueValue":{
                              "id":"uniqueValue",
                              "name":"鍵值資料",
                              "value":"002020051300002",
                              "type":"string",
                              "format":"n/a"
                           },
                           "uniqueField":{
                              "id":"uniqueField",
                              "name":"鍵值名稱",
                              "value":"PNO",
                              "type":"string",
                              "format":"n/a"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"keys"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data 
```json
{
    "status": "success",
    "message": [
        "查無資料"
    ],
    "data": {
        "HRFlowList": {
            "name": "CA4.行政服務單簽核-待簽核列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "HRFlowList"
        }
    }
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
