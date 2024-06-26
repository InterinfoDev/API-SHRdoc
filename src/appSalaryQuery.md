# appSalaryQuery
取得指定年月、員工薪資條明細資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSalaryQuery
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {salaryYM:202111 companyId:TW , salaryCount:1 , key:32262008498747441193712198021232260366087649257856381618231} | Object | 查詢條件 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas 取消empid傳入，改用getUser
        "salaryYM":"202111",
        "companyId":"TW", 
        "salaryCount":1,
        "key":"32262008498747441193712198021232260366087649257856381618231",
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
| salaryYM | 202111 | String | 薪資年月 | Y | AC(YYYYmm) |
| companyId | TW | String | 公司代號 | Y | n/a |
| salaryCount | 1 | Integer | 發薪次數 | Y | n/a |
| key | 32262008498747441193712198021232260366087649257856381618231 | String | 通行金鑰 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salary":{  --lucas 改名
         "id":"salary", --lucas 改名
         "name":"薪資資訊",
         "value":{
            "salaryYM":{  --lucas改名
               "id":"salaryYM", --lucas改名
               "name":"薪資年月",
               "value":"202109",
               "type":"string",
               "format":"YYYYmm"
            },
            "count":{
               "id":"count",
               "name":"計薪次數",
               "value":1,
               "type":"integer",
               "format":"count"
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
         "name":"員工資訊", --lucas 改名
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
            "companyFullName": {
               "name": "公司全名",
               "type": "string",
               "value": "XXXX公司",
               "format": "n/a",
               "id": "companyFullName"
            },
            "grade":{
               "id":"grade",
               "name":"職等",
               "value":"07",
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
      "attend":{
         "id":"attend", --lucas 改名
         "name":"考勤資訊",
         "value":[
            {
               "id":"04",
               "name":"假別資訊",
               "value":{
                  "vacatCode":{
                     "id":"vacatCode",
                     "name":"假別代號",
                     "value":"04",
                     "type":"string",
                     "format":"n/a"
                  },
                  "vacatName":{
                     "id":"vacatName",
                     "name":"假別名稱",
                     "value":"補休假",
                     "type":"string",
                     "format":"n/a"
                  },
                  "vacatHour":{
                     "id":"vacatHour",
                     "name":"假別時數",
                     "value":4.5,
                     "type":"decimal",
                     "format":"hour"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"09",
               "name":"假別資訊",
               "value":{
                  "vacatCode":{
                     "id":"vacatCode",
                     "name":"假別代號",
                     "value":"09",
                     "type":"string",
                     "format":"n/a"
                  },
                  "vacatName":{
                     "id":"vacatName",
                     "name":"假別名稱",
                     "value":"特休假",
                     "type":"string",
                     "format":"n/a"
                  },
                  "vacatHour":{
                     "id":"vacatHour",
                     "name":"假別時數",
                     "value":3.25,
                     "type":"decimal",
                     "format":"hour"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "due":{
         "id":"due", --lucas 改名
         "name":"應領資訊",
         "value":[
            {
               "id":"A01",
               "name":"薪資項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"薪資項目代號",
                     "value":"A01",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"薪資項目名稱",
                     "value":"本薪",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"薪資項目金額",
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
               "name":"薪資項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"薪資項目代號",
                     "value":"A02",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"薪資項目名稱",
                     "value":"伙食津貼",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"薪資項目金額",
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
         "id":"deduct", --lucas改名
         "name":"減項資訊",
         "value":[
            {
               "id":"B01",
               "name":"薪資項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"薪資項目代號",
                     "value":"B01",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"薪資項目名稱",
                     "value":"請假扣款",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"薪資項目金額",
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
               "name":"薪資項目明細",
               "value":{
                  "salNo":{
                     "id":"salNo",
                     "name":"薪資項目代號",
                     "value":"B02",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salName":{
                     "id":"salName",
                     "name":"薪資項目名稱",
                     "value":"福利金",
                     "type":"string",
                     "format":"n/a"
                  },
                  "salAmount":{
                     "id":"salAmount",
                     "name":"薪資項目金額",
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
         "id":"total", --lucas改名
         "name":"核給資訊",
         "value":[
            {
               "id":"due",
               "name":"應領小計資訊", --lucas改名
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
               "name":"應扣小計資訊", --lucas改名
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
               "name":"實領資訊", --lucas改名
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
         "id":"notes", --lucas改名
         "name":"其他補充事項",
         "value":[
            {
               "id":"workDayOverHour",
               "name":"加班資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"平日給薪時數",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":10,
                     "type":"decimal",
                     "format":"hour"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"holidayOverHour",
               "name":"加班資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"假日給薪時數",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":5,
                     "type":"decimal",
                     "format":"hour"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"familySupport",
               "name":"扶養眷屬資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"扶養眷屬",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":1,
                     "type":"integer",
                     "format":"people"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"healthSupport",
               "name":"扶養健保眷屬資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"健保眷屬",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":1,
                     "type":"integer",
                     "format":"people"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"approveLeave",
               "name":"特休資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"今年度特休核休",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":15,
                     "type":"decimal",
                     "format":"day"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"usedLeave",
               "name":"特休資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"今年度特休已休",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":5,
                     "type":"decimal",
                     "format":"day"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"untakenLeave",
               "name":"特休資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"今年度特休未休",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":10,
                     "type":"decimal",
                     "format":"day"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"overdue",
               "name":"特休資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"逾期特休",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":2,
                     "type":"decimal",
                     "format":"day"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"personalCurrentPeriod",
               "name":"退休金資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"個人本期提撥新制退休金",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":3500,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "id":"companyCurrentPeriod", --lucas修正
               "name":"退休金資訊",
               "value":{
                  "title":{
                     "id":"title",
                     "name":"其他補充事項標頭",
                     "value":"公司本期提撥新制退休金",
                     "type":"string",
                     "format":"n/a"
                  },
                  "content":{
                     "id":"content",
                     "name":"其他補充事項內容",
                     "value":3500,
                     "type":"decimal",
                     "format":"currency"
                  }
               },
               "type":"object",
               "format":"n/a"
            },
            {
               "name":"退休金資訊",
               "type":"object",
               "format":"n/a",
               "id":"totalCurrentPeriod",
               "value":{
                  "content":{
                     "name":"其他補充事項內容",
                     "type":"decimal",
                     "value":30.0,
                     "format":"currency",
                     "id":"content"
                  },
                  "title":{
                     "name":"其他補充事項標頭",
                     "type":"string",
                     "value":"本期提撥合計",
                     "format":"n/a",
                     "id":"title"
                  }
               }
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "YYYYmm":"西元年月",
            "YYYYmmdd":"西元年月日",
            "hour":"小時",
            "day":"天",
            "currency":"元",
            "people":"人",
            "count":"次數",
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
   "status":"success",  --lucas 修改架構
   "message":[
      "回傳成功"
   ],
   "data":{
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
