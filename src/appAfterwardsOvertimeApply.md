# appAfterwardsOvertimeApply
新增事後加班單畫面所需要的資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAfterwardsOvertimeApply
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
| request | {empid:xxx} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin"
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

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "properties": {
            "format": {
                "hour": "小時",
                "n/a": ""
            }
        },
        "overtime": {
            "name": "當月加班資訊",
            "type": "array",
            "value": [
                {
                    "name": "加班總時數",
                    "type": "object",
                    "value": {
                        "note": {
                            "name": "n/A",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "note"
                        },
                        "describe": {
                            "name": "描述標題",
                            "type": "string",
                            "value": "當月已申請加班總時數",
                            "format": "n/a",
                            "id": "describe"
                        },
                        "value": {
                            "name": "總時數",
                            "type": "decimal",
                            "value": 0.0,
                            "format": "hour",
                            "id": "value"
                        }
                    },
                    "format": "n/a",
                    "id": "overAmt"
                },
                {
                    "name": "加班給薪時數",
                    "type": "object",
                    "value": {
                        "note": {
                            "name": "n/A",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "note"
                        },
                        "describe": {
                            "name": "描述標題",
                            "type": "string",
                            "value": "當月已申請加班給薪時數",
                            "format": "n/a",
                            "id": "describe"
                        },
                        "value": {
                            "name": "給薪時數",
                            "type": "decimal",
                            "value": 0.0,
                            "format": "hour",
                            "id": "value"
                        }
                    },
                    "format": "n/a",
                    "id": "overPayHour"
                },
                {
                    "name": "加班補休時數",
                    "type": "object",
                    "value": {
                        "note": {
                            "name": "n/A",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "note"
                        },
                        "describe": {
                            "name": "描述標題",
                            "type": "string",
                            "value": "當月已申請加班補休時數",
                            "format": "n/a",
                            "id": "describe"
                        },
                        "value": {
                            "name": "補休時數",
                            "type": "decimal",
                            "value": 0.0,
                            "format": "hour",
                            "id": "value"
                        }
                    },
                    "format": "n/a",
                    "id": "overRestHour"
                }
            ],
            "format": "n/a",
            "id": "overtime"
        },
        "note": {
            "name": "n/A",
            "type": "string",
            "value": "",
            "format": "n/a",
            "id": "note"
        },
        "applyForm": {
            "name": "加班單申請",
            "type": "object",
            "value": {
                "overtimeDate": {
                    "name": "事後加班日期",
                    "type": "string",
                    "value": "20240108",
                    "format": "YYYYmmdd",
                    "id": "overtimeDate"
                }
            },
            "format": "n/a",
            "id": "applyForm"
        }
    }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，不會有查無資料情況
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "查無資料"
    ],
    "data": {}
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
