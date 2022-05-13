# appFlowAgentList
查詢簽核代理人資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowAgentList
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
| request | {'cpnyid':'TW' ,'empid':'admin' ,'func_name':'' ,'dept_no':'' ,'agent':''} | Object | 查詢條件(依據使用者所選擇要查看的公司、員工、代理功能、部門、簽核代理人，取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cpnyid":"TW", 
        "empid":"admin", 
        "func_name":"",
        "dept_no":"",
        "agent":""
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
| cpnyid | TW | String | 公司別 | N | n/a |
| empid | admin | String | 員工編號 | N | n/a |
| func_name |  | String | 代理功能 | N | n/a |
| dept_no |  | int | 部門 | N | n/a |
| agent |  | String | 簽核代理人 | N | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "flowAgentList":{
         "name":"簽核代理人列表",
         "type":"array",
         "value":[
            {
               "name":"簽核代理人資訊",
               "type":"object",
               "value":{
                  "function":{
                     "name":"代理功能",
                     "type":"string",
                     "value":"C.126.個人工作目標修改簽核",
                     "format":"n/a",
                     "id":"function"
                  },
                  "endTime":{
                     "name":"代理結束時間",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"endTime"
                  },
                  "agent":{
                     "name":"代理人",
                     "type":"string",
                     "value":"11000021",
                     "format":"n/a",
                     "id":"agent"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系統管理員",
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
                  "starTime":{
                     "name":"代理起始時間",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"starTime"
                  },
                  "agentName":{
                     "name":"簽核代理人姓名",
                     "type":"string",
                     "value":"薪O條",
                     "format":"n/a",
                     "id":"agentName"
                  }
               },
               "format":"n/a",
               "id":"flowAgent"
            },
            {
               "name":"簽核代理人資訊",
               "type":"object",
               "value":{
                  "function":{
                     "name":"代理功能",
                     "type":"string",
                     "value":"C.221.績效考核表簽核",
                     "format":"n/a",
                     "id":"function"
                  },
                  "endTime":{
                     "name":"代理結束時間",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"endTime"
                  },
                  "agent":{
                     "name":"代理人",
                     "type":"string",
                     "value":"10600009",
                     "format":"n/a",
                     "id":"agent"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系統管理員",
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
                  "starTime":{
                     "name":"代理起始時間",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"starTime"
                  },
                  "agentName":{
                     "name":"簽核代理人姓名",
                     "type":"string",
                     "value":"tOs",
                     "format":"n/a",
                     "id":"agentName"
                  }
               },
               "format":"n/a",
               "id":"flowAgent"
            },
            {
               "name":"簽核代理人資訊",
               "type":"object",
               "value":{
                  "function":{
                     "name":"代理功能",
                     "type":"string",
                     "value":"CB2.1.請假單簽核",
                     "format":"n/a",
                     "id":"function"
                  },
                  "endTime":{
                     "name":"代理結束時間",
                     "type":"string",
                     "value":"2022/01/17 17:00",
                     "format":"n/a",
                     "id":"endTime"
                  },
                  "agent":{
                     "name":"代理人",
                     "type":"string",
                     "value":"11000021",
                     "format":"n/a",
                     "id":"agent"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系統管理員",
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
                  "starTime":{
                     "name":"代理起始時間",
                     "type":"string",
                     "value":"2022/01/17 08:00",
                     "format":"n/a",
                     "id":"starTime"
                  },
                  "agentName":{
                     "name":"簽核代理人姓名",
                     "type":"string",
                     "value":"薪O條",
                     "format":"n/a",
                     "id":"agentName"
                  }
               },
               "format":"n/a",
               "id":"flowAgent"
            },
            {
               "name":"簽核代理人資訊",
               "type":"object",
               "value":{
                  "function":{
                     "name":"代理功能",
                     "type":"string",
                     "value":"CB3.7.補刷卡簽核",
                     "format":"n/a",
                     "id":"function"
                  },
                  "endTime":{
                     "name":"代理結束時間",
                     "type":"string",
                     "value":"2022/01/21 17:00",
                     "format":"n/a",
                     "id":"endTime"
                  },
                  "agent":{
                     "name":"代理人",
                     "type":"string",
                     "value":"10804025",
                     "format":"n/a",
                     "id":"agent"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系統管理員",
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
                  "starTime":{
                     "name":"代理起始時間",
                     "type":"string",
                     "value":"2022/01/21 08:00",
                     "format":"n/a",
                     "id":"starTime"
                  },
                  "agentName":{
                     "name":"簽核代理人姓名",
                     "type":"string",
                     "value":"TOs",
                     "format":"n/a",
                     "id":"agentName"
                  }
               },
               "format":"n/a",
               "id":"flowAgent"
            },
            {
               "name":"簽核代理人資訊",
               "type":"object",
               "value":{
                  "function":{
                     "name":"代理功能",
                     "type":"string",
                     "value":"CB3.7.補刷卡簽核",
                     "format":"n/a",
                     "id":"function"
                  },
                  "endTime":{
                     "name":"代理結束時間",
                     "type":"string",
                     "value":"2022/01/21 17:00",
                     "format":"n/a",
                     "id":"endTime"
                  },
                  "agent":{
                     "name":"代理人",
                     "type":"string",
                     "value":"11000021",
                     "format":"n/a",
                     "id":"agent"
                  },
                  "empFullName":{
                     "name":"員工中文姓名",
                     "type":"string",
                     "value":"系統管理員",
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
                  "starTime":{
                     "name":"代理起始時間",
                     "type":"string",
                     "value":"2022/01/21 08:00",
                     "format":"n/a",
                     "id":"starTime"
                  },
                  "agentName":{
                     "name":"簽核代理人姓名",
                     "type":"string",
                     "value":"薪O條",
                     "format":"n/a",
                     "id":"agentName"
                  }
               },
               "format":"n/a",
               "id":"flowAgent"
            }
         ],
         "format":"n/a",
         "id":"flowAgentList"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "day":"天",
            "n/a":""
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
