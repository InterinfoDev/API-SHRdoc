# appSalaryRecent
取得某員工最近一次薪資發放資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSalaryRecent
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
| request | {key:32262008498747441193712198021232260366087649257856381618231} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --lucas移除 empid，改用getUser
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
| key | 32262008498747441193712198021232260366087649257856381618231 | String | 通行金鑰 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salaryRecent":{
         "id":"salaryRecent", --lucas 改名
         "name":"最近一次薪資發放資訊",
         "value":{ 
            "companyId":{
               "name": "公司代號",
               "type": "string",
               "value": "TECXMN",
               "format": "n/a",
               "id": "companyId"
            },
            "salaryYM":{ --lucas 改名
               "id":"salaryYM", --lucas 改名
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
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，將帶出系統年月與登入者公司等預設資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "salaryRecent":{
         "name":"最近一次薪資發放資訊",
         "type":"object",
         "value":{
            "companyId":{
               "name":"公司代號",
               "type":"string",
               "value":"1",
               "format":"n/a",
               "id":"companyId"
            },
            "salaryYM":{
               "name":"薪資年月",
               "type":"string",
               "value":"202405",
               "format":"YYYYmm",
               "id":"salaryYM"
            },
            "count":{
               "name":"計薪次數",
               "type":"integer",
               "value":1,
               "format":"count",
               "id":"count"
            },
            "indate":{
               "name":"入帳日期",
               "type":"string",
               "value":"20240531",
               "format":"YYYYmmdd",
               "id":"indate"
            }
         },
         "format":"n/a",
         "id":"salaryRecent"
      }
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
