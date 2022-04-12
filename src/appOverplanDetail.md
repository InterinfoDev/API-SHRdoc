# appOverplanDetail
查詢該預定加班單詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOverplanDetail
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
| request | {pno:W002022011900001, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的預定加班單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "pno":"W002022011900001", 
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
| pno | W002022011900001 | String | 單據編號 | Y | n/a |
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
            "n/a":""
         }
      },
      "flowHistory":{
         "name":"流程紀錄",
         "type":"object",
         "value":{
            "historyKey":{
               "name":"流程鍵值",
               "type":"string",
               "value":"4018143326273716525552090972897090755341893430474685977954583012953934710584411029083038347111585967840458166001489548654179235360456151",
               "format":"n/a",
               "id":"historyKey"
            }
         },
         "format":"n/a",
         "id":"flowHistory"
      },
      "overplanDetail":{
         "name":"預定加班單詳細資訊",
         "type":"object",
         "value":{
            "totalPayHour":{
               "name":"總計給薪時數",
               "type":"decimal",
               "value":0.0,
               "format":"hour",
               "id":"totalPayHour"
            },
            "amt":{
               "name":"總計",
               "type":"decimal",
               "value":4.0,
               "format":"hour",
               "id":"amt"
            },
            "beforeWork":{
               "name":"跨日往前加班",
               "type":"boolean",
               "value":false,
               "format":"hour",
               "id":"beforeWork"
            },
            "stime":{
               "name":"起始時間",
               "type":"string",
               "value":"1900",
               "format":"HHmm",
               "id":"stime"
            },
            "pno":{
               "name":"單據編號",
               "type":"string",
               "value":"W002022011900001",
               "format":"n/a",
               "id":"pno"
            },
            "sdate":{
               "name":"起始日期",
               "type":"string",
               "value":"20220119",
               "format":"YYYYmmdd",
               "id":"sdate"
            },
            "uploadFiles":{
               "name":"附件資訊",
               "type":"array",
               "value":[
                  
               ],
               "format":"n/a",
               "id":"uploadFiles"
            },
            "etime":{
               "name":"結束時間",
               "type":"string",
               "value":"2300",
               "format":"HHmm",
               "id":"etime"
            },
            "edate":{
               "name":"結束日期",
               "type":"string",
               "value":"20220119",
               "format":"YYYYmmdd",
               "id":"edate"
            },
            "oldEatUnit":{
               "name":"原用餐時間",
               "type":"decimal",
               "value":0.0,
               "format":"hour",
               "id":"oldEatUnit"
            },
            "applicant":{
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
               "id":"applicant"
            },
            "note":{
               "name":"加班內容",
               "type":"string",
               "value":"TTTT",
               "format":"n/a",
               "id":"note"
            },
            "totalRestHour":{
               "name":"總計補休時數",
               "type":"decimal",
               "value":4.0,
               "format":"hour",
               "id":"totalRestHour"
            },
            "eatYN":{
               "name":"是否用餐",
               "type":"boolean",
               "value":false,
               "format":"hour",
               "id":"eatYN"
            },
            "employee":{
               "name":"人事基本資料",
               "type":"object",
               "value":{
                  "depCode":{
                     "name":"部門代號",
                     "type":"string",
                     "value":"14122",
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
                     "value":"L1線B班",
                     "format":"n/a",
                     "id":"depFullName"
                  },
                  "empFullEname":{
                     "name":"員工英文姓名",
                     "type":"string",
                     "value":"test_Ename",
                     "format":"n/a",
                     "id":"empFullEname"
                  }
               },
               "format":"n/a",
               "id":"employee"
            },
            "newEatUnit":{
               "name":"新用餐時間",
               "type":"decimal",
               "value":0.0,
               "format":"hour",
               "id":"newEatUnit"
            },
            "payType":{
               "name":"給付方式",
               "type":"object",
               "value":{
                  "payTypeCode":{
                     "name":"給付方式代碼",
                     "type":"string",
                     "value":"A",
                     "format":"n/a",
                     "id":"payTypeCode"
                  },
                  "payTypeName":{
                     "name":"給付方式名稱",
                     "type":"string",
                     "value":"補休",
                     "format":"n/a",
                     "id":"payTypeName"
                  }
               },
               "format":"n/a",
               "id":"payType"
            }
         },
         "format":"n/a",
         "id":"overplanDetail"
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
