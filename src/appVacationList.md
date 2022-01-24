# appVacationList
查詢單一員工該年月區間的請假資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationList
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| request | {vacationYM:202201, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的員工及畫面上的年月取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "vacationYM":"202201", 
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
| vacationYM | 202201 | String | 查詢年月 | Y | AC(YYYYmm) |
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
         "name":"個人請假列表",
         "type":"object",
         "value":{
            "vacationYM":{
               "name":"請假年月",
               "type":"string",
               "value":"202201",
               "format":"YYYYmm",
               "id":"vacationYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "userInfo":{
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
            "photo":{
               "name":"員工相片",
               "type":"string",
               "value":"",
               "format":"base64",
               "id":"photo"
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
               "value":"admin000",
               "format":"n/a",
               "id":"empFullEname"
            }
         },
         "format":"n/a",
         "id":"userInfo"
      },
      "vacationList":{
         "name":"個人請假列表",
         "type":"array",
         "value":[
            {
               "name":"請假資訊",
               "type":"object",
               "value":{
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
                  "pno":{
                     "name":"單據編號",
                     "type":"string",
                     "value":"W00202201220001",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "sdate":{
                     "name":"起始日期",
                     "type":"string",
                     "value":"20220121",
                     "format":"YYYYmmdd",
                     "id":"sdate"
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
                     "value":"20220121",
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
                  "hkindd":{
                     "name":"子假別資訊",
                     "type":"object",
                     "value":{
                        "hcoded":{
                           "name":"子假別代碼",
                           "type":"string",
                           "value":"00",
                           "format":"n/a",
                           "id":"hcoded"
                        },
                        "hcdname":{
                           "name":"子假別名稱",
                           "type":"string",
                           "value":"例假",
                           "format":"n/a",
                           "id":"hcdname"
                        }
                     },
                     "format":"n/a",
                     "id":"hkindd"
                  }
               },
               "format":"n/a",
               "id":"vacationInfo"
            },
            {
               "name":"請假資訊",
               "type":"object",
               "value":{
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
                  "pno":{
                     "name":"單據編號",
                     "type":"string",
                     "value":"W00202201220002",
                     "format":"n/a",
                     "id":"pno"
                  },
                  "sdate":{
                     "name":"起始日期",
                     "type":"string",
                     "value":"20220110",
                     "format":"YYYYmmdd",
                     "id":"sdate"
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
                     "value":"20220110",
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
                  "hkindd":{
                     "name":"子假別資訊",
                     "type":"object",
                     "value":{
                        "hcoded":{
                           "name":"子假別代碼",
                           "type":"string",
                           "value":"00",
                           "format":"n/a",
                           "id":"hcoded"
                        },
                        "hcdname":{
                           "name":"子假別名稱",
                           "type":"string",
                           "value":"例假",
                           "format":"n/a",
                           "id":"hcdname"
                        }
                     },
                     "format":"n/a",
                     "id":"hkindd"
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
            "HHmm":"時間時分",
            "hour":"小時",
            "base64":"Base64編碼格式",
            "YYYYmmdd":"西元年月日",
            "day":"天",
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
