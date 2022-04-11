# appFlowHistory
取得該筆單據流程紀錄

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowHistory
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
| request | {flowHis:xxx} | Object | 由各個Detail回傳的flowHis取得 |

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "flowHis":"225721252929321375615416977232747178356918537416530009027085451609431956050312438342049846696219313403435868271166793"
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
| flowHis | 225721252929321375615416977232747178356918537416530009027085451609431956050312438342049846696219313403435868271166793 | String | 流程紀錄鍵值 | Y | n/a |


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
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "HHmmss":"時間時分秒"
         }
      },
      "flowHistory":{
         "name":"流程紀錄",
         "type":"array",
         "value":[
            {
               "name":"簽核節點資訊",
               "type":"object",
               "value":{
                  "memo":{
                     "name":"簽核意見",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"memo"
                  },
                  "approveTime":{
                     "name":"簽核時間",
                     "type":"string",
                     "value":"110401",
                     "format":"HHmmss",
                     "id":"approveTime"
                  },
                  "approver":{
                     "name":"簽核人員",
                     "type":"array",
                     "value":[
                        {
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
                        }
                     ],
                     "format":"n/a",
                     "id":"approver"
                  },
                  "agent":{
                     "name":"代理人員",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"agent"
                  },
                  "approveYN":{
                     "name":"是否核准",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"approveYN"
                  },
                  "finishYN":{
                     "name":"是否歸檔",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"finishYN"
                  },
                  "approveDate":{
                     "name":"簽核日期",
                     "type":"string",
                     "value":"20210806",
                     "format":"YYYYmmdd",
                     "id":"approveDate"
                  },
                  "level":{
                     "name":"流程關卡",
                     "type":"string",
                     "value":"待處理",
                     "format":"n/a",
                     "id":"level"
                  }
               },
               "format":"n/a",
               "id":"flowLevel"
            },
            {
               "name":"簽核節點資訊",
               "type":"object",
               "value":{
                  "memo":{
                     "name":"簽核意見",
                     "type":"string",
                     "value":"",
                     "format":"n/a",
                     "id":"memo"
                  },
                  "approveTime":{
                     "name":"簽核時間",
                     "type":"string",
                     "value":"",
                     "format":"HHmmss",
                     "id":"approveTime"
                  },
                  "approver":{
                     "name":"簽核人員",
                     "type":"array",
                     "value":[
                        {
                           "empFullName":{
                              "name":"員工中文姓名",
                              "type":"string",
                              "value":"岑O祐",
                              "format":"n/a",
                              "id":"empFullName"
                           },
                           "empid":{
                              "name":"員工編號",
                              "type":"string",
                              "value":"1783",
                              "format":"n/a",
                              "id":"empid"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"approver"
                  },
                  "agent":{
                     "name":"代理人員",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"agent"
                  },
                  "approveYN":{
                     "name":"是否核准",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"approveYN"
                  },
                  "finishYN":{
                     "name":"是否歸檔",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"finishYN"
                  },
                  "approveDate":{
                     "name":"簽核日期",
                     "type":"string",
                     "value":"",
                     "format":"YYYYmmdd",
                     "id":"approveDate"
                  },
                  "level":{
                     "name":"流程關卡",
                     "type":"string",
                     "value":"代理人",
                     "format":"n/a",
                     "id":"level"
                  }
               },
               "format":"n/a",
               "id":"flowLevel"
            }
         ],
         "format":"n/a",
         "id":"flowHistory"
      }
   }
}
```

### HTTP Response when No Data 
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
