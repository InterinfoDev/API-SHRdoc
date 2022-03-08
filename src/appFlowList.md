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
| request | {key:xxx} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "key":"640130555211610131235169414143042796600194383642310910304424435998404931445693"
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
| key | 640130555211610131235169414143042796600194383642310910304424435998404931445693 | String | 鍵值 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "HRFlowList":{
         "name":"CA3. My Profile-待簽核列表",
         "type":"array",
         "value":[
            {
               "name":"No.1",
               "type":"object",
               "value":{
                  "fields":{
                     "name":"欄位資訊",
                     "type":"array",
                     "value":[
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"72英特內全名(中和)",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"單據編號",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"14121 L1線A班",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"公司別",
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
                              "value":"單位",
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
                              "value":"員工編號",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20220126",
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
                              "value":"185832",
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
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"002022012600001",
                              "format":"HHmmss",
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
                     "id":"fields"
                  },
                  "keys":{
                     "name":"欄位鍵值",
                     "type":"array",
                     "value":[
                        {
                           "uniqueValue":{
                              "name":"鍵值資料",
                              "type":"string",
                              "value":"002022012600001",
                              "format":"n/a",
                              "id":"uniqueValue"
                           },
                           "uniqueField":{
                              "name":"鍵值名稱",
                              "type":"string",
                              "value":"PNO_PROV",
                              "format":"n/a",
                              "id":"uniqueField"
                           }
                        },
                        {
                           "uniqueValue":{
                              "name":"鍵值資料",
                              "type":"string",
                              "value":"admin",
                              "format":"n/a",
                              "id":"uniqueValue"
                           },
                           "uniqueField":{
                              "name":"鍵值名稱",
                              "type":"string",
                              "value":"EMPID",
                              "format":"n/a",
                              "id":"uniqueField"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"keys"
                  },
                  "signFlow":{
                     "name":"簽核資訊",
                     "type":"object",
                     "value":{
                        "approveUrl":{
                           "name":"簽核網址",
                           "type":"string",
                           "value":"http://114.34.125.246:8090/servlet/jform?file=hrm8w.pkg&init_func=CA3.個人資料維護覆核&locale=TW&uid=admin&pwd=EM.SESSION.625050713326173689566150008254964663313715735618087650126089349876075207877230&em_flowkey=002022012600001,admin",
                           "format":"hyperlink",
                           "id":"approveUrl"
                        }
                     },
                     "format":"n/a",
                     "id":"signFlow"
                  }
               },
               "format":"n/a",
               "id":"0"
            }
         ],
         "format":"n/a",
         "id":"HRFlowList"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "HHmmss":"時間時分秒",
            "hyperlink":"超連結"
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
            "name": "CB2.3.假單銷假簽核-待簽核列表",
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
