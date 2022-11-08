# appIrregularOvertimeApply
加班異常欄位預設值

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimeApply
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


### JSON representation
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326", 
   "right":"51341911904173543336756162544864820",
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "查詢成功"
    ],
    "data": {
        "queryCondition": {
            "name": "查詢預帶資料",
            "type": "object",
            "value": {
                "beforeMins": {
                    "name": "提前多久刷卡視為異常",
                    "type": "integer",
                    "value": 30,
                    "format": "min",
                    "id": "beforeMins"
                },
                "viewTypeName": {
                    "name": "顯示種類名稱",
                    "type": "string",
                    "value": "顯示所有異常",
                    "format": "n/a",
                    "id": "viewTypeName"
                },
                "viewType": {
                    "name": "顯示種類代號",
                    "type": "string",
                    "value": "A",
                    "format": "n/a",
                    "id": "viewType"
                },
                "outMins": {
                    "name": "刷卡時間超過多久未報加班視為異常",
                    "type": "integer",
                    "value": 30,
                    "format": "min",
                    "id": "outMins"
                },
                "afterMins": {
                    "name": "延後多久刷卡視為異常",
                    "type": "integer",
                    "value": 30,
                    "format": "min",
                    "id": "afterMins"
                }
            },
            "format": "n/a",
            "id": "queryCondition"
        },
        "properties": {
            "format": {
                "min": "分鐘",
                "n/a": ""
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
