# appPushSetting
查詢通知設定

### HTTP Request
https://114.34.125.246:8090/servlet/HRNative/appPushSetting

### HTTP Request Method
POST

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |

### JSON representation
Here is a JSON representation of request.
json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820"
}

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### HTTP Response when Successful
json
{
   "status":"success",
   "message":[
      "查詢成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "setting":{
         "name":"設定資訊",
         "type":"object",
         "value":{
            "notifyFlag":{
               "name":"通知功能",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"notifyFlag"
            }
         },
         "format":"n/a",
         "id":"setting"
      }
   }
}

### HTTP Response when Failed
json
{
    "status": "fail",
    "code": 500,
    "message": [
        "XXX"
    ],
    "data": {}
}

### HTTP Response when Exception
json
{
    "status": "fail",
    "code": 406,
    "message": [
        "XXX"
    ],
    "data": {}
}
