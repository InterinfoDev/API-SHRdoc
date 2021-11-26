# appAttendDetail

取得指定年月、員工薪資條明細資訊

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appSalaryQuery
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
| request | {salaryYM:202104, empid:admin , salaryCount:1 , salaryPwd:123457334} | Object | 查詢條件


### JSON representation

Here is a JSON representation of request.

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "salaryYM":"202104", 
        "salaryCount":"1",
        "salaryPwd":"123457334",
        "empid":"admin"
    }
}
```


### Properties

| Property | Type | Description |
|:---------|:-----|:------------|
| **uid**   | String | 加密後帳號 |
| **right** | String | 加密後系統相關資料 |
| **request** | 要求本文 |

### request Properties

| Key | Value | Type | Description
|:----------|:-------------|:-----|:------------|
| salaryYM | 202104 | String | 薪資年月 |
| salaryCount | 1 | String | 發薪次數 |
| salaryPwd | 123457334 | String | 薪資條密碼 |
| empid | admin | String | 員工編號 |


### HTTP Response when Successful
```json
{
	{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "id":"salaryInfo",
         "name":"薪資資訊",
         "value":{
            "ym":{
               "id":"ym",
               "name":"薪資年月",
               "value":"202109",
               "type":"string",
               "format":"YYYYmm"
            },
            "count":{
               "id":"count",
               "name":"計薪次數",
               "value":"1",
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
      "personal":{
         "id":"personalInfo",
         "name":"個人資訊",
         "value":{
            "photo":{
               "id":"photo",
               "name":"員工照片",
               "value":"dataurl",
               "type":"base64",
               "format":"n/a"
            },
            "empName":{
               "id":"empName",
               "name":"員工中文姓名",
               "value":"林奇杰",
               "type":"string",
               "format":"n/a"
            },
            "empEname":{
               "id":"empEname",
               "name":"員工英文姓名",
               "value":"Lucas",
               "type":"string",
               "format":"n/a"
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
            "depName":{
               "id":"depName",
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
         "id":"attendInfo",
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
         "id":"salaryDueInfo",
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
         "id":"salaryDeductInfo",
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
         "id":"totalInfo",
         "name":"核給資訊",
         "value":[
            {
               "id":"due",
               "name":"小計資訊",
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
               "name":"小計資訊",
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
               "name":"小計資訊",
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
         "id":"otherNotes",
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
               "id":"personalCurrentPeriod",
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

### HTTP Response when Failed
```json
{
    "status": "fail",
    "code": 406,
    "message": [
        "系統錯誤"
    ],
    "data": {}
}
```