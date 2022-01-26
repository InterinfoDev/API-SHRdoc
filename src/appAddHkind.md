# appAddHkind
取得新增畫面假別的下拉選項

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAddHkind
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
| request | {} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
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
                     "value":"",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"",
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
                     "value":"例假-有事情",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"00.TW2",
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
                     "value":"產假-懷孕未滿兩個月流產",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08-TW.01",
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
                     "value":"產假-懷孕兩至三個月流產",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08-TW.02",
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
                     "value":"半薪病假-八週-妊娠六個月以上分娩者",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08.05",
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
                     "value":"半薪病假-四週-妊娠三個月以上未滿六個月流產者",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08.TW6",
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
                     "value":"半薪病假-一週-妊娠二個月以上未滿三個月流產者，不給工資",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08.TW7",
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
                     "value":"半薪病假-五日-妊娠未滿二個月流產者，不給工資",
                     "format":"n/a",
                     "id":"hcname"
                  },
                  "hcode":{
                     "name":"假別代碼",
                     "type":"string",
                     "value":"08.TW8",
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