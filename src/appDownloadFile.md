# appDownloadFile
檔案下載

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appDownloadFile
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
| request | {fileKey:xxxxx} | Object | 查詢條件

### JSON representation

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "fileKey":"xxxxx"
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
| Case No | Key | Value | Type | Description | Required | Format |
|:----------|:----------|:-------------|:-----|:------------|:------------|:------------|
| 1 | fileKey | 202112 | String | 檔案序號 | Y | n/a |

### HTTP Response when Successful
成功將直接顯示檔案blob，請務必參考content type

### HTTP Response when No Data
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "查無檔案"
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
