# appPersonalDataMaintenance
個人資料維護異動

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPersonalDataMaintenance
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
| request | {fieldId:"id",fieldValue:"test_value"} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{"editField":[
    {"fieldId":"108617422147704250851","fieldValue":["test_Ename"]}
    ,{"fieldId":"106141291729238904091","fieldValue":["94929570122831101032"]}]}
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
| editField | fieldId,fieldValue | Object | 欄位代號 | Y | n/a | 異動欄位 |
| fieldId | xxxxxxxxxxx | String | 欄位代號 | Y | n/a | 加密過後的欄位ID |
| fieldValue | xxxxxxxxxxx | String | 欄位資料 | Y | n/a | 異動資料 |

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
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
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
