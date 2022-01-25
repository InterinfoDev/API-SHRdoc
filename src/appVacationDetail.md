# appVacationDetail
查詢該假單詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationDetail
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
| request | {pno:W00202201250001, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的假單單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "pno":"W00202201250001", 
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
| pno | W00202201250001 | String | 單據編號 | Y | n/a |
| empid | admin | String | 員工編號 | Y | n/a |


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
            "HHmm":"時間時分",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "day":"天",
            "n/a":""
         }
      },
      "vacationDetail":{
         "name":"假單詳細資訊",
         "type":"object",
         "value":{
            "apprdate":{
               "name":"生效日期",
               "type":"string",
               "value":"",
               "format":"YYYYmmdd",
               "id":"apprdate"
            },
            "jobDeputyInfo":{
               "name":"職務代理人資訊",
               "type":"object",
               "value":{
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"薪O條",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"11000021",
                     "format":"n/a",
                     "id":"empid"
                  }
               },
               "format":"n/a",
               "id":"jobDeputyInfo"
            },
            "amt":{
               "name":"總計",
               "type":"decimal",
               "value":8.0,
               "format":"hour",
               "id":"amt"
            },
            "stime":{
               "name":"起始時間",
               "type":"string",
               "value":"0800",
               "format":"HHmm",
               "id":"stime"
            },
            "hkind":{
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
            "pno":{
               "name":"單據編號",
               "type":"string",
               "value":"W00202201250001",
               "format":"n/a",
               "id":"pno"
            },
            "sdate":{
               "name":"起始日期",
               "type":"string",
               "value":"20220117",
               "format":"YYYYmmdd",
               "id":"sdate"
            },
            "uploadFiles":{
               "name":"附件資訊",
               "type":"array",
               "value":[
                  {
                     "fileType":{
                        "name":"檔案類型",
                        "type":"string",
                        "value":"",
                        "format":"n/a",
                        "id":"fileType"
                     },
                     "fileUrl":{
                        "name":"檔案路徑",
                        "type":"string",
                        "value":"8394768758650934487139215644085449220561352994877809057609795881391964303976063959390413861765306620980509412090431956792262100059547268421208875708309193001476077621211220788276621789810786481552460035435218638029708026615307257983",
                        "format":"n/a",
                        "id":"fileUrl"
                     },
                     "fileName":{
                        "name":"檔案名稱",
                        "type":"string",
                        "value":"1643078742185_【台壽】(MP1100171)TPSYNC-特休資料拋轉外掛(SD)(1).docx",
                        "format":"n/a",
                        "id":"fileName"
                     }
                  },
                  {
                     "fileType":{
                        "name":"檔案類型",
                        "type":"string",
                        "value":"image/jpeg",
                        "format":"n/a",
                        "id":"fileType"
                     },
                     "fileUrl":{
                        "name":"檔案路徑",
                        "type":"string",
                        "value":"213054348471705645522899686059682058334332468666904109085709401572564865917840459407644865526610519454919698294050221",
                        "format":"n/a",
                        "id":"fileUrl"
                     },
                     "fileName":{
                        "name":"檔案名稱",
                        "type":"string",
                        "value":"1643078742200_A.jpg",
                        "format":"n/a",
                        "id":"fileName"
                     }
                  },
                  {
                     "fileType":{
                        "name":"檔案類型",
                        "type":"string",
                        "value":"application/pdf",
                        "format":"n/a",
                        "id":"fileType"
                     },
                     "fileUrl":{
                        "name":"檔案路徑",
                        "type":"string",
                        "value":"455081326282139220778915637967543067724210186456599314554053797322699112004686013661897571284512146408289108883247131030352506479918432248519610045402377780797371013561698903045297101962589301299762891115085188159",
                        "format":"n/a",
                        "id":"fileUrl"
                     },
                     "fileName":{
                        "name":"檔案名稱",
                        "type":"string",
                        "value":"1643078742200_1642650962408_任09歡迎新同事-1110120.pdf",
                        "format":"n/a",
                        "id":"fileName"
                     }
                  }
               ],
               "format":"n/a",
               "id":"uploadFiles"
            },
            "approveDeputyInfo":{
               "name":"簽核代理人資訊",
               "type":"array",
               "value":[
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  },
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  },
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  },
                  {
                     "empFullName":{
                        "name":"員工中文姓名",
                        "type":"string",
                        "value":"薪O條",
                        "format":"n/a",
                        "id":"empFullName"
                     },
                     "empid":{
                        "name":"員工編號",
                        "type":"string",
                        "value":"11000021",
                        "format":"n/a",
                        "id":"empid"
                     }
                  }
               ],
               "format":"n/a",
               "id":"approveDeputyInfo"
            },
            "etime":{
               "name":"結束時間",
               "type":"string",
               "value":"1700",
               "format":"HHmm",
               "id":"etime"
            },
            "edate":{
               "name":"結束日期",
               "type":"string",
               "value":"20220117",
               "format":"YYYYmmdd",
               "id":"edate"
            },
            "applicantInfo":{
               "name":"申請人資訊",
               "type":"object",
               "value":{
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系O管",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  }
               },
               "format":"n/a",
               "id":"applicantInfo"
            },
            "note":{
               "name":"備註",
               "type":"string",
               "value":"20220125KevinTestTest",
               "format":"n/a",
               "id":"note"
            },
            "delayNote":{
               "name":"逾期請假原因",
               "type":"string",
               "value":"20220125KevinTestTestLateLate",
               "format":"n/a",
               "id":"delayNote"
            },
            "spectialDate":{
               "name":"特殊日期",
               "type":"string",
               "value":"",
               "format":"YYYYmmdd",
               "id":"spectialDate"
            },
            "userInfo":{
               "name":"人事基本資料",
               "type":"object",
               "value":{
                  "depCode":{
                     "name":"部門代號",
                     "type":"string",
                     "value":"14121",
                     "format":"n/a",
                     "id":"depCode"
                  },
                  "companyId":{
                     "name":"公司代號",
                     "type":"string",
                     "value":"TW",
                     "format":"n/a",
                     "id":"companyId"
                  },
                  "companyFullName":{
                     "name":"公司全名",
                     "type":"string",
                     "value":"72英特內全名(中和)",
                     "format":"n/a",
                     "id":"companyFullName"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系O管",
                     "format":"n/a",
                     "id":"empFullName"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "depFullName":{
                     "name":"部門名稱",
                     "type":"string",
                     "value":"L1線A班",
                     "format":"n/a",
                     "id":"depFullName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"EEadmin",
                     "format":"n/a",
                     "id":"empFullEname"
                  }
               },
               "format":"n/a",
               "id":"userInfo"
            },
            "hkindd":{
               "name":"子假別資訊",
               "type":"object",
               "value":{
                  "hcoded":{
                     "name":"子假別代碼",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"hcoded"
                  },
                  "hcdname":{
                     "name":"子假別名稱",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"hcdname"
                  }
               },
               "format":"n/a",
               "id":"hkindd"
            }
         },
         "format":"n/a",
         "id":"vacationDetail"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
