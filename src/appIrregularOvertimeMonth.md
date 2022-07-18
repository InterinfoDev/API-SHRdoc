# appIrregularOvertimeMonth
取得加班異常資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimeMonth
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
| request | {empid:[admin],cpnyid:TW,irragularYM:202207,skind:A,before:30,after:30,uncard:30,depNumber:[1]} | Object | 查詢條件(depNumber/empid至少選一輸入)

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":["admin"], 
        "cpnyid":"TW",
        "irragularYM":"202207",
        "skind":"A",
        "before":30,
        "after":30,
        "uncard":30,
        "depNumber":["1"]
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
| empid | admin | Array(String) | 員工編號 | N | n/a |
| cpnyid | TW | String | 公司代號 | Y | n/a |
| irragularYM | 202207 | String | 查詢年月 | Y | AC(YYYYmm) |
| skind | A | String | 顯示種類 | Y | n/a |
| before | 30 | Integer | 提前多久刷卡視為異常 | Y | n/a |
| after | 30 | Integer | 延後多久刷卡視為異常 | Y | n/a |
| uncard | 30 | Integer | 刷卡時間超過多久未報加班視為異常 | Y | n/a |
| depNumber | [1] | Array(String) | 部門代號 | N | n/a |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "main": {
            "name": "加班異常資訊",
            "type": "object",
            "value": {
                "irragularYM": {            --richard 修改名稱irragularYM
                    "name": "加班異常年月",
                    "type": "string",
                    "value": "202207",
                    "format": "YYYYmm",
                    "id": "irragularYM"     --richard 修改名稱irragularYM
                }
            },
            "format": "n/a",
            "id": "main"
        },
        "IrregularOvertimeList": {
            "name": "員工加班異常列表",
            "type": "array",
            "value": [
                {
                    "name": "員工加班異常資訊",
                    "type": "object",
                    "value": {
                        "position": {
                            "name": "職稱",
                            "type": "string",
                            "value": "系統管理員",
                            "format": "n/a",
                            "id": "position"
                        },
                        "count": {
                            "name": "異常筆數",
                            "type": "integer",
                            "value": 5,
                            "format": "count",
                            "id": "count"
                        },
                        "empFullName": {
                            "name": "員工中文姓名",
                            "type": "string",
                            "value": "系統管理員",
                            "format": "n/a",
                            "id": "empFullName"
                        },
                        "empid": {
                            "name": "員工編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "empid"
                        },
                        "depFullName": {
                            "name": "部門名稱",
                            "type": "string",
                            "value": "英特內股份有限公司",
                            "format": "n/a",
                            "id": "depFullName"
                        }
                    },
                    "format": "n/a",
                    "id": "IrregularOvertimeInformation"
                }
            ],
            "format": "count",
            "id": "IrregularOvertimeList"
        },
        "properties": {
            "format": {
                "count": "數量",
                "n/a": "",
                "YYYYmm": "西元年月"
            }
        }
    }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
