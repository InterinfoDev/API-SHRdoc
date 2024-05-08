# appEmployeePhoto
取得特定員工照片資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appEmployeePhoto
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
| request | { empid:admin } | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin"
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
| empid | admin | String | 員工編號 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "personal":{
         "id":"personal", --lucas 修改
         "name":"個人資訊",
         "value":{
            "empid":{
               "id":"empid",
               "name":"員工編號",
               "value":"L100387",
               "type":"string",
               "format":"n/a"
            },
            "photo":{       -- richard 格式修改
               "id":"photo",
               "name":"員工照片",
               "value": "http://59.124.100.151:8090/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f055d5e5d46535051635956535a4c637d0d110e11d794b4dabeb8daa991630e0909080c08070b0c080e0b0760485e4b5a4d6b4a4d4b535a11554f58",
              "format": "hyperlink",
               "type":"string"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "properties":{    -- richard 格式修改 
         "format":{
            "hyperlink":"超連結",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Photo Data
若有查到使用者，但使用者沒有照片時候，回傳空白
```json
{  --lucas 增加新的可能
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "personal":{
         "id":"personal", --lucas 修改
         "name":"個人資訊",
         "value":{
            "empid":{
               "id":"empid",
               "name":"員工編號",
               "value":"L100387",
               "type":"string",
               "format":"n/a"
            },
            "photo":{       -- richard 格式修改
               "id":"photo",
               "name":"員工照片",
               "value":"",
               "type":"string",
               "format":"hyperlink"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "properties":{        -- richard 格式修改
         "format":{
            "hyperlink":"超連結",
            "n/a":""
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
