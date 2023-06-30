# appFunctionRight 
取得員工APP功能資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFunctionRight
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 拿掉empid傳入，改用getUser()
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

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "appRight":{
         "id":"appRight",
         "name":"功能設定資料",
         "value":[
            {
               "id":"1",
               "name":"功能資料",
               "value":{
                  "functionKey":{
                     "name":"功能編號",
                     "type":"string",
                     "value":"3e27729c-9847-4e4d-8167-d1badb377f64",
                     "format":"n/a",
                     "id":"functionKey"
                  },
                  "functionName":{
                     "id":"functionName",
                     "name":"功能名稱",
                     "value":"公告資料",
                     "type":"string",
                     "format":"n/a"
                  },
                  "functionEnName":{
                     "id":"functionEnName",
                     "name":"功能英文名稱",
                     "value":"System Publish",
                     "type":"string",
                     "format":"n/a"
                  },
                  "functionDisplayName":{
                     "name":"顯示功能名稱",
                     "type":"string",
                     "value":"員工請假",
                     "format":"n/a",
                     "id":"functionDisplayName"
                  },
                  "permission":{
                     "id":"permission",
                     "name":"是否有權限",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "isWebview":{
                     "id":"isWebview",
                     "name":"是否為WebView功能",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "webViewSrc":{
                     "id":"webViewSrc",
                     "name":"webView網址",
                     "value":"/servlet/jform?file=xxxx&init_func=A1",
                     "type":"string",
                     "format":"hyperlink"
                  },
                  "webViewImg":{
                     "name":"webView圖片代號",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"webViewImg"
                  },
                  "visible":{
                     "id":"visible",
                     "name":"是否顯示",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "hyperlink":"超連結",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
通常使用者一定會有資料，若無資料代表無權限使用APP，拋出500錯誤
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
