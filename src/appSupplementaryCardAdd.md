# appSupplementaryCardAdd
員工考勤補卡

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardAdd
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
| request | {"empid":"admin","cardType":"I","cardDate":"20220217","cardTime":"1857","reasonCode":"001","note":"忘記帶卡","file":""} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin",
      "cardType":"I",
      "cardDate":"20220217",
      "cardTime":"1857",
      "reasonCode":"001",
      "note":"忘記帶卡",
      "file":""
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| empid | admin | String | 員工編號 | Y | n/a | 異動欄位 |
| cardType | I/O | String | 補卡別 | Y | n/a | 進卡:I,出卡:O |
| cardDate | 20220217 | String | 補卡日期 | Y | n/a | AC(YYYYmmdd) |
| cardTime | 1857 | String | 補卡時間 | Y | n/a | TIME(HHmm) |
| reasonCode | 001 | String | 補卡原因代碼 | Y | n/a | 根據原因設定檔的代碼 |
| note | 忘記帶卡 | String | 備註 | Y | n/a | 補卡原因 |
| file |  | String | 附件檔案 | Y | base64 | 補卡附件 |

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
                "n/a": ""
            }
        },
        "supplementaryCardData": {
            "name": "新增補卡資料",
            "type": "object",
            "value": {
                "executeMessage": {
                    "name": "異動訊息",
                    "type": "string",
                    "value": "該時間已申請過補登，請勿重覆申請",
                    "format": "n/a",
                    "id": "executeMessage"
                },
                "executeResult": {
                    "name": "異動結果",
                    "type": "boolean",
                    "value": false,
                    "format": "n/a",
                    "id": "executeResult"
                }
            },
            "format": "n/a",
            "id": "supplementaryCardData"
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
