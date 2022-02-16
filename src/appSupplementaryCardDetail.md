# appSupplementaryCardDetail
查詢該補假詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardDetail
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
| request | {supplementaryCardKey:20210600000000000002} | Object | 查詢條件(依據使用者所選擇要查看的假單單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "supplementaryCardKey":"20210600000000000002"
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
| supplementaryCardKey | 20210600000000000002 | String | 單據編號 | Y | n/a |

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
                "HHmm": "時間時分",
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        },
        "supplementaryCardDetail": {
            "name": "補卡詳細資訊",
            "type": "object",
            "value": {
                "addDate": {
                    "name": "申請日期",
                    "type": "string",
                    "value": "20210629",
                    "format": "YYYYmmdd",
                    "id": "addDate"
                },
                "file": {
                    "name": "附件檔案",
                    "type": "string",
                    "value": {
                        "fileType": {
                            "name": "檔案類型",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "fileType"
                        },
                        "fileUrl": {
                            "name": "檔案路徑",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "fileUrl"
                        },
                        "fileName": {
                            "name": "檔案名稱",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "fileName"
                        }
                    },
                    "format": "n/a",
                    "id": "file"
                },
                "empid": {
                    "name": "員工編號",
                    "type": "string",
                    "value": "admin",
                    "format": "n/a",
                    "id": "empid"
                },
                "approvalStatus": {
                    "name": "簽核狀態",
                    "type": "string",
                    "value": "未生效",
                    "format": "n/a",
                    "id": "approvalStatus"
                },
                "reason": {
                    "name": "補登原因",
                    "type": "string",
                    "value": "忘刷卡",
                    "format": "n/a",
                    "id": "reason"
                },
                "cardDate": {
                    "name": "補卡日期",
                    "type": "string",
                    "value": "20210601",
                    "format": "YYYYmmdd",
                    "id": "cardDate"
                },
                "cardTime": {
                    "name": "補卡時間",
                    "type": "string",
                    "value": "0600",
                    "format": "HHmm",
                    "id": "cardTime"
                },
                "note": {
                    "name": "備註",
                    "type": "string",
                    "value": "忘刷卡",
                    "format": "n/a",
                    "id": "note"
                },
                "empFullName": {
                    "name": "員工中文姓名",
                    "type": "string",
                    "value": "系O管",
                    "format": "n/a",
                    "id": "empFullName"
                },
                "depCode": {
                    "name": "部門明碼",
                    "type": "string",
                    "value": "14121",
                    "format": "n/a",
                    "id": "depCode"
                }
            },
            "format": "n/a",
            "id": "supplementaryCardDetail"
        }
    }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
