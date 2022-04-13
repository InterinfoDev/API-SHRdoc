# appVacationApply
新增預定加班單畫面所需要的資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOverplanApply
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
| request | {overplanDate:xxx} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "overplanDate":"20220413"
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
| overplanDate | 20220413 | String | 預定加班日期 | Y | n/a |


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
            "type": "object",
            "value": {
                "overAmt": {
                    "name": "加班總時數",
                    "type": "object",
                    "value": {
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
                "overRestHour": {
                    "name": "加班補休時數",
                    "type": "object",
                    "value": {
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
                },
                "overPayHour": {
                    "name": "加班給薪時數",
                    "type": "object",
                    "value": {
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
                }
            },
            "format": "n/a",
            "id": "overtime"
        },
        "note": {
            "name": "備註",
            "type": "object",
            "value": "備註：預定加班單申請完30天內須申請實際加班單，若逾期，則視同放棄。",
            "format": "n/a",
            "id": "note"
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
