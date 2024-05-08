# appLogout
記錄使用者登出資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appLogout
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
| request | {deviecId:TEST_DEVICE_ID} | Object | 異動條件

### JSON representation
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "deviecId":"TEST_DEVICE_ID"
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
| deviecId | TEST_DEVICE_ID | 裝置識別碼 | 欄位代號 | Y | n/a |  |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "logout":{
         "name":"登出記錄異動", 
         "type":"object",
         "value":{
            "logoutTime":{
               "name":"登出時間",
               "type":"string",
               "value":"1843",
               "format":"HHmm",
               "id":"logoutTime"
            },
            "logoutDate":{
               "name":"登出日期",
               "type":"string",
               "value":"20220318",
               "format":"YYYYmmdd",
               "id":"logoutDate"
            }
         },
         "format":"n/a",
         "id":"logout"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料，除非驗證失敗
```json
{
    "status": "fail",
    "code": 500,
    "message": [
        "登出失敗"
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
