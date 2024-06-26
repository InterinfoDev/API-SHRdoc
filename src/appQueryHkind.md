# appQueryHkind
取得查詢條件假別的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appQueryHkind
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
| request | {empid:[admin], companyId:TW} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "companyId":"TW",
        "empid":["admin"]
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
| companyId | TW | String | 公司代號 | N | n/a |
| empid | [admin] | Array(String) | 員工編號 | N | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "hkindOption":{
         "name":"假別選項",
         "type":"array",
         "value":[
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"例假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"00",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"休息",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"000",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"事假中和",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"01",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"半薪病假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"產假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08-TW",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"年假(特休)",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"09",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"調休",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"10",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"加班補休",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"15",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"出差假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"20",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"遲到",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"34",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"公司福利假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"39",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"half半薪病假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"54",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"mc生理假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"55",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"事假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"60",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"71補休",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"71",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"72年假",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"72",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            },
            {
               "name":"假別資訊",
               "type":"object",
               "value":{
                  "hcname":{
                     "name":"假別名稱",
                     "type":"string",
                     "value":"73特休",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"73",
                     "format":"n/a",
                     "id":"hcode"
                  }
               },
               "format":"n/a",
               "id":"hkind"
            }
         ],
         "format":"n/a",
         "id":"hkindOption"
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
無資料則屬於資料異常，不太可能沒有下拉選項
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
