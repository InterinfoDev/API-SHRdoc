# appIrregularOvertimePDF
取得員工加班異常名單PDF

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appIrregularOvertimePDF
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
| request | {"empid":"admin","irragularYM":"202207","viewType":"A","beforeMins":30,"afterMins":30,"outMins":30} | Object | 查詢條件

### JSON representation

```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin",
      "irragularYM":"202207",
      "viewType":"A",
      "beforeMins":30,
      "afterMins":30,
      "outMins":30
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
| empid | admin | String | 員工編號 | N | n/a |
| irragularYM | 202207 | String | 查詢年月 | N | n/a |
| viewType | A | String | 顯示種類 | Y | n/a |
| beforeMins | 30 | Integer | 提前多久刷卡視為異常 | Y | n/a |
| afterMins | 30 | Integer | 延後多久刷卡視為異常 | Y | n/a |
| outMins | 30 | Integer | 刷卡時間超過多久未報加班視為異常 | Y | n/a |

### HTTP Response when Successful
成功將直接顯示檔案blob，請務必參考content type

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
