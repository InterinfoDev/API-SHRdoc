# appQueryVacation
取得系統年月、員工請假資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQueryVacation
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

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
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
                     "value":"applytest001",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"integer",
                     "value":2,
                     "format":"count",
                     "id":"approved"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"depFullName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"HOWAREU",
                     "format":"n/a",
                     "id":"empFullEname"
                  }
               },
               "format":"n/a",
               "id":"vacationInfo"
            }
         ],
         "format":"n/a",
         "id":"vacationList"
      },
      "properties":{
         "format":{
            "base64":"Base64編碼格式",
            "count":"數量",
            "n/a":"",
            "YYYYmm":"西元年月"
         }
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "main":{
      "name":"請假年月",
      "type":"string",
      "value":"202205",
      "format":"YYYYmm",
      "id":"vacationYM"
   },
   "vacationList":{
      "name":"員工請假列表",
      "type":"array",
      "value":[],
      "format":"n/a",
      "id":"vacationList"
   },
   "properties":{
      "format":{
         "base64":"Base64編碼格式",
         "count":"數量",
         "n/a":"",
         "YYYYmm":"西元年月"
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
