# appSetting
取得設定資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSetting
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
| request | {} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
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

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "resetPincode": {
            "name": "重置PINCODE",
            "type": "boolean",
            "value": true,
            "format": "n/a",
            "id": "resetPincode"
        },
        "properties": {
            "format": {
                "n/a": ""
            }
        },
        "useBinding": {
            "name": "是否開啟綁定功能",
            "type": "boolean",
            "value": true,
            "format": "n/a",
            "id": "useBinding"
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
