# appPinCode
驗證識別碼取得設定資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPinCode
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {pinCode:970909} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "request":{
        "pinCode":"970909", 
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
| pinCode | 970909 | String | 員工編號 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "pinCode":{
         "name":"驗證資訊",
         "type":"object",
         "value":{
            "validationResult":{
               "name":"驗證結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"validationResult"
            },
            "errorMessage":{
               "name":"錯誤訊息",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"errorMessage"
            },
            "companyFullName":{
               "name":"公司名稱",
               "type":"string",
               "value":"英特內軟體",
               "format":"n/a",
               "id":"companyFullName"
            },
            "file":{
               "name":"設定檔案",
               "type":"string",
               "value":"hrm8w.pkg",
               "format":"n/a",
               "id":"file"
            },
            "domain":{
               "name":"設定網域",
               "type":"string",
               "value":"http://www.interinfo.com.tw",
               "format":"n/a",
               "id":"domain"
            },
            "language":{
               "name":"設定語系",
               "type":"string",
               "value":"TW",
               "format":"n/a",
               "id":"language"
            }
         },
         "format":"n/a",
         "id":"pinCode"
      }
   }
}
```

### HTTP Response when No Data 
無資料屬於正常情況
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "pinCode":{
         "name":"驗證資訊",
         "type":"object",
         "value":{
            "validationResult":{
               "name":"驗證結果",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"validationResult"
            },
            "errorMessage":{
               "name":"錯誤訊息",
               "type":"string",
               "value":"查無資料",
               "format":"n/a",
               "id":"errorMessage"
            },
            "companyFullName":{
               "name":"公司名稱",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"companyFullName"
            },
            "file":{
               "name":"設定檔案",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"file"
            },
            "domain":{
               "name":"設定網域",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"domain"
            },
            "language":{
               "name":"設定語系",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"language"
            }
         },
         "format":"n/a",
         "id":"pinCode"
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
