# appSalbondQuery
取得指定年月、員工獎金條明細資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSalbondQuery
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
| request | {salbondYM:202111, indate:20211115, key:32262008498747441193712198021232260366087649257856381618231} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 取消empid傳入，改用getUser
        "salbondYM":"202111", 
        "indate":"20211115",
        "key":"32262008498747441193712198021232260366087649257856381618231"
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
| salbondYM | 202111 | String | 薪資年月 | Y | AC(YYYYmm) |
| indate | 20211115 | String | 入帳日期 | Y | AC(YYYYmmdd) |
| key | 32262008498747441193712198021232260366087649257856381618231 | String | 通行金鑰 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salbond":{ --lucas 改名
         "id":"salbond", --lucas 改名
         "name":"獎金資訊",
         "value":{
            "salbondYM":{ --lucas 改名
               "id":"salbondYM", --lucas 改名
               "name":"獎金年月",
               "value":"202109",
               "type":"string",
               "format":"YYYYmm"
            },
            "indate":{
               "id":"indate",
               "name":"入帳日期",
               "value":"20211105",
               "type":"string",
               "format":"YYYYmmdd"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "employee":{ --lucas 改名
         "id":"employee", --lucas 改名
         "name":"員工資訊",  --lucas 改名
         "value":{
            "empFullName":{ --lucas 改名
               "id":"empFullName", --lucas 改名
               "name":"員工中文姓名",
               "value":"林奇杰",
               "type":"string",
               "format":"n/a"
            },
            "empFullEname":{ --lucas 改名
               "id":"empFullEname", --lucas 改名
               "name":"員工英文姓名",
               "value":"Lucas",
               "type":"string",
               "format":"n/a"
            },
            "depCode":{
               "id":"depCode",
               "name":"部門代碼",
               "value":"D3000",
               "type":"string",
               "format":"n/a"
            },
            "depFullName":{ --lucas 改名
               "id":"depFullName", --lucas 改名
               "name":"部門名稱",
               "value":"CTO",
               "type":"string",
               "format":"n/a"
            },
            "companyFullName":{
               "id":"companyFullName",
               "name":"公司全名",
               "value":"XXXX公司",
               "type":"string",
               "format":"n/a"
            },
            "empid":{
               "id":"empid",
               "name":"員工編號",
               "value":"L100387",
               "type":"string",
               "format":"n/a"
            },
            "position":{
               "id":"position",
               "name":"職稱",
               "value":"CTO",
               "type":"string",
               "format":"n/a"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "due":{
         "id":"due", --lucas 改名
         "name":"應領資訊",
         "value":[
            {
               "id":"A01",
               "name":"獎金項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"獎金項目代號",
                     "value":"A01",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"獎金項目名稱",
                     "value":"本薪",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"獎金項目金額",
                     "value":30000,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "format":"n/a",
               "type":"object"
            },
            {
               "id":"A02",
               "name":"獎金項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"獎金項目代號",
                     "value":"A02",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"獎金項目名稱",
                     "value":"伙食津貼",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"獎金項目金額",
                     "value":2400,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "type":"decimal",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "deduct":{ 
         "id":"deduct", --lucas 改名
         "name":"減項資訊",
         "value":[
            {
               "id":"B01",
               "name":"獎金項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"獎金項目代號",
                     "value":"B01",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"獎金項目名稱",
                     "value":"請假扣款",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"獎金項目金額",
                     "value":500,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "format":"n/a",
               "type":"object"
            },
            {
               "id":"B02",
               "name":"獎金項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"獎金項目代號",
                     "value":"B02",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"獎金項目名稱",
                     "value":"福利金",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"獎金項目金額",
                     "value":350,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "format":"n/a",
               "type":"object"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "total":{
         "id":"total", --lucas 改名
         "name":"核給資訊",
         "value":[
            {
               "id":"due",
               "name":"應領小計資訊", --lucas 改名
               "value":{
                  "paidNo":{
                     "id":"paidNo",
                     "name":"小計項目標題",
                     "value":"應領金額",
                     "type":"string",
                     "format":"n/a"
                  },
                  "paidAmount":{
                     "id":"paidAmount",
                     "name":"小計項目金額",
                     "value":32000,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "format":"n/a",
               "type":"object"
            },
            {
               "id":"deduct",
               "name":"應扣小計資訊", --lucas 改名
               "value":{
                  "paidNo":{
                     "id":"paidNo",
                     "name":"小計項目標題",
                     "value":"應扣金額",
                     "type":"string",
                     "format":"n/a"
                  },
                  "paidAmount":{
                     "id":"paidAmount",
                     "name":"小計項目金額",
                     "value":2800,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "format":"n/a",
               "type":"object"
            },
            {
               "id":"current",
               "name":"實領小計資訊", --lucas 改名
               "value":{
                  "paidNo":{
                     "id":"paidNo",
                     "name":"小計項目標題",
                     "value":"實領金額",
                     "type":"string",
                     "format":"n/a"
                  },
                  "paidAmount":{
                     "id":"paidAmount",
                     "name":"小計項目金額",
                     "value":28800,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "format":"n/a",
               "type":"object"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "notes":{
         "id":"notes", --lucas 改名
         "name":"其他補充事項(預留空間)",
         "value":[
            
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "YYYYmm":"西元年月",
            "YYYYmmdd":"西元年月日",
            "currency":"元",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],  --lucas 修改架構
   "data":{}
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
