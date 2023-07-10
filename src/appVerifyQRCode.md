# appVerifyQRCode
驗證QRCODE資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVerifyQRCode
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
| request | {qrCodeImg:657200235561417569,employeeId:admin} | Object | 查詢條件

### JSON representation
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "qrCodeImg":"657200235561417569",
        "employeeId":"admin"
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
 Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| qrCodeImg | 657200235561417569 | String | QRCODE的資訊 | N | n/a |
| employeeId | admin | String | 登入者 | N | n/a |
### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "驗證完成"
   ],
   "data":{
      "address":{
         "name":"ip位置",
         "type":"string",
         "value":"192.168.10.112",
         "format":"n/a",
         "id":"address"
      },
      "properties":{
         "format":{
            "n/a":""
         }
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
