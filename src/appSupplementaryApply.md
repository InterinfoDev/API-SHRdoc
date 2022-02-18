# appSupplementaryApply
取得補卡資訊與當天班別資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryApply
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
| request | {empid:admin , date:20220214} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin", 
        "date":"20220214",
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
| empid | admin | String | 員工編號 | Y | n/a |
| date | 20220214 | String | 查詢日期 | Y | AC(YYYYmmdd) |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "employee":{
         "name":"員工資訊",
         "type":"object",
         "value":{
            "depCode":{
               "name":"部門代號",
               "type":"string",
               "value":"14121",
               "format":"n/a",
               "id":"depCode"
            },
            "companyFullName":{
               "name":"公司全名",
               "type":"string",
               "value":"72英特內全名(中和)",
               "format":"n/a",
               "id":"companyFullName"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "empFullName":{
               "name":"員工中文姓名",
               "type":"string",
               "value":"系O管",
               "format":"n/a",
               "id":"empFullName"
            },
            "empFullEname":{
               "name":"員工英文姓名",
               "type":"string",
               "value":"test_Ename",
               "format":"n/a",
               "id":"empFullEname"
            },
            "depFullName":{
               "name":"部門名稱",
               "type":"string",
               "value":"L1線A班",
               "format":"n/a",
               "id":"depFullName"
            }
         },
         "format":"n/a",
         "id":"employee"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "supplementary":{
         "name":"補卡資訊",
         "type":"object",
         "value":{
            "workOff":{
               "name":"下班時間",
               "type":"string",
               "value":"1700",
               "format":"HHmm",
               "id":"workOff"
            },
            "workOn":{
               "name":"上班時間",
               "type":"string",
               "value":"0800",
               "format":"HHmm",
               "id":"workOn"
            },
            "lastCard":{
               "name":"最後打卡時間",
               "type":"string",
               "value":"1700",
               "format":"HHmm",
               "id":"lastCard"
            },
            "firstCard":{
               "name":"最早打卡時間",
               "type":"string",
               "value":"0800",
               "format":"HHmm",
               "id":"firstCard"
            },
            "workDate":{
               "name":"班別日期",
               "type":"string",
               "value":"20220214",
               "format":"YYYYmmdd",
               "id":"workDate"
            }
         },
         "format":"n/a",
         "id":"supplementary"
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
