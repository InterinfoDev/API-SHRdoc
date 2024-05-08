# appPersonalDataMaintenance
個人資料維護異動

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPersonalDataMaintenance
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
| request | {"editField":[{"fieldId":"xxxx","fieldValue":["xxx"]}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "editField":[
         {
            "fieldId":"xxx",
            "fieldValue":[
               "test"
            ]
         }
      ]
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| editField |  | Array(String) | 修改欄位 | Y | n/a | 異動欄位資訊 |
| fieldId |  | Strin) | 欄位代號 | Y | n/a | 異動欄位代號 |
| fieldValue |  | String | 修改內容 | Y | n/a | 異動欄位內容 |

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
            "n/a":""
         }
      },
      "personalData":{
         "name":"異動個人資料",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"異動成功",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
            },
            "isFlow":{
               "name":"是否有簽核單據",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"isFlow"
            }
         },
         "format":"n/a",
         "id":"personalData"
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
