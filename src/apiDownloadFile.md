# apiDownloadFile
檔案下載

### HTTP Request
```
http://59.124.100.151:8090/servlet/apiM/shiftAPP/V1/interfaces/apiDownloadFile
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過apiLogin取得
| right | 51341911904173543336756162544864820 | String | 需透過apiLogin取得 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "requestHeader": {
  },
  "requestBody": {
    "fileKey":"xxxxx"
  },
  "uid":"98599308101484732326",
  "right":"51341911904173543336756162544864820"
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| requestHeader | Object | 要求本文 |
| requestBody | Object | 要求本文 |

### requestBody Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| fileKey | xxxxxx | String | 檔案序號 | Y | n/a |

### requestBody FieldName
| FieldName | Description |
|:----------|:-------------|
| resultMessage | 結果訊息 |
| resultCode | 結果代號 |
| message | 訊息 |

### HTTP Response when Successful
成功將直接顯示檔案blob，請務必參考content type

### HTTP Response when Failed
```json
{
   "responseHeader":{
      "resultMessage":"查無檔案",
      "resultCode":"500"
   },
   "responseBody":{
      
   }
}
```

### HTTP Response when Exception
```json
{
    "responseHeader": {
        "resultMessage": "xxxxx",
        "resultCode": "406"
    },
    "responseBody": {
    }
}
```
