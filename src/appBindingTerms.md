# appBindingTerms
查詢綁定協議內容

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBindingTerms
```

### HTTP Request Mehod
```
POST
```


### Request body
| Property | Type | Description |
|:---------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {locale:TW} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "locale":"TW",
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
| locale | TW | String | 語系 | N | n/a |

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
      "bindingTerms":{
         "name":"法條資訊",
         "type":"object",
         "value":{
            "termsContent":{
               "name":"法條內文",
               "type":"string",
               "value":"我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!我是通用公司別條款!!",
               "format":"n/a",
               "id":"termsContent"
            }
         },
         "format":"n/a",
         "id":"bindingTerms"
      }
   }
}
```

### HTTP Response when No Data
無資料則顯示設定檔資料或是預設資料
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "name": "綁定狀態資訊",
        "properties": {
            "format": {
                "n/a": ""
            }
        },
        "type": "object",
        "value": {
            "level": {
                "name": "綁定機制",
                "type": "integer",
                "value": 1,
                "format": "n/a",
                "id": "level"
            }
        },
        "format": "n/a",
        "id": "bindingInformation"
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
