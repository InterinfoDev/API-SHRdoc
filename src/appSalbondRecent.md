# appSalbondRecent
取得某員工最近一次獎金發放資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSalbondRecent
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
| request | {empid:admin, key:32262008498747441193712198021232260366087649257856381618231} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "key":"32262008498747441193712198021232260366087649257856381618231"
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
| empid | admin | String | 員工編號 | Y | n/a |
| key | 32262008498747441193712198021232260366087649257856381618231 | String | 通行金鑰 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salbondRecent":{
         "id":"salbondRecentInfo",
         "name":"最近一次獎金發放資訊",
         "value":{
            "ym":{
               "id":"ym",
               "name":"獎金年月",
               "value":"202109",
               "type":"string",
               "format":"YYYYmm"
            },
            "indate":{
               "id":"indate",
               "name":"入帳日期",
               "value":"20211105",
               "type":"string",
               "format":"YYYYmmdd"
            }
         },
         "type":"object",
         "format":"n/a"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{}
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
