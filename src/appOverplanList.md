# appOverplanList
查詢單一員工該年月區間的預定加班資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOverplanList
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
| request | {overplanYM:202201, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的員工及畫面上的年月取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "overplanYM":"202201", 
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
| overplanYM | 202201 | String | 查詢年月 | Y | AC(YYYYmm) |
| empid | admin | String | 員工編號 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"個人預定加班",
         "type":"object",
         "value":{
            "overplanYM":{
               "name":"預定加班年月",
               "type":"string",
               "value":"202201",
               "format":"YYYYmm",
               "id":"overplanYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "overplanList":{
         "name":"個人預定加班列表",
         "type":"array",
         "value":[
            {
               "name":"預定加班資訊",
               "type":"object",
               "value":{
                  "amt":{
                     "name":"總計",
                     "type":"decimal",
                     "value":4.0,
                     "format":"hour",
                     "id":"amt"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
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
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approved"
                  },
                  "used":{
                     "name":"已申請實際",
                     "type":"string",
                     "value":"否",
                     "format":"n/a",
                     "id":"used"
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
               "id":"overplan"
            },
            {
               "name":"預定加班資訊",
               "type":"object",
               "value":{
                  "amt":{
                     "name":"總計",
                     "type":"decimal",
                     "value":2.0,
                     "format":"hour",
                     "id":"amt"
                  },
                  "empid":{
                     "name":"員工編號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"empid"
                  },
                  "stime":{
                     "name":"起始時間",
                     "type":"string",
                     "value":"1800",
                     "format":"HHmm",
                     "id":"stime"
                  },
                  "pno":{
                     "name":"單據編號",
                     "type":"string",
                     "value":"W002022012400001",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "sdate":{
                     "name":"起始日期",
                     "type":"string",
                     "value":"20220124",
                     "format":"YYYYmmdd",
                     "id":"sdate"
                  },
                  "etime":{
                     "name":"結束時間",
                     "type":"string",
                     "value":"2000",
                     "format":"HHmm",
                     "id":"etime"
                  },
                  "edate":{
                     "name":"結束日期",
                     "type":"string",
                     "value":"20220124",
                     "format":"YYYYmmdd",
                     "id":"edate"
                  },
                  "approved":{
                     "name":"已生效",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approved"
                  },
                  "used":{
                     "name":"已申請實際",
                     "type":"string",
                     "value":"否",
                     "format":"n/a",
                     "id":"used"
                  },
                  "payType":{
                     "name":"給付方式",
                     "type":"object",
                     "value":{
                        "payTypeCode":{
                           "name":"給付方式代碼",
                           "type":"string",
                           "value":"B",
                           "format":"n/a",
                           "id":"payTypeCode"
                        },
                        "payTypeName":{
                           "name":"給付方式名稱",
                           "type":"string",
                           "value":"給薪",
                           "format":"n/a",
                           "id":"payTypeName"
                        }
                     },
                     "format":"n/a",
                     "id":"payType"
                  }
               },
               "format":"n/a",
               "id":"overplan"
            }
         ],
         "format":"n/a",
         "id":"overplanList"
      },
      "employee":{
         "name":"員工基本資料",
         "type":"object",
         "value":{
            "position":{
               "name":"職稱",
               "type":"string",
               "value":"系統管理員",
               "format":"n/a",
               "id":"position"
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
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "YYYYmm":"西元年月"
         }
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
