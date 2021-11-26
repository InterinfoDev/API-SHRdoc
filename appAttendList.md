# appAttendList

取得考勤列表資訊

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appAttendList
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
| request | {'deptNumber':'1', 'attendYM':'202104', 'empid':'', 'companyId':'1'} | Object | 查詢條件


### JSON representation

Here is a JSON representation of request.

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "attendYM":"202104", 
        "companyId":"97090920",
        "deptNumber":"1",
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
| attendYM | 202104 | String | 查詢年月 |
| companyId | 97090920| String | 公司別代號 |
| deptNumber | 1 | String | 部門代號 |
| empid | admin| String | 員工編號 |


### HTTP Response when Successful
```json
{
   "data":{
      "main":{
         "id":"attendInfo",
         "name":"考勤資訊列表",
         "value":{
            "ym":{
               "id":"ym",
               "name":"考勤年月",
               "value":"202110",
               "type":"string",
               "format":"YYYYmm"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "attend":{
         "id":"attend",
         "name":"考勤列表資訊",
         "value":[
            {
               "id":"attendDetail",
               "name":"個人、考勤資訊",
               "value":{
                  "empid":{
                     "id":"empid",
                     "name":"員工編號",
                     "value":"L100387",
                     "type":"string",
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
                  "depCode":{
                     "id":"depCode",
                     "name":"部門代號",
                     "value":"D2000",
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
                  "isAbnormal":{
                     "id":"isAbnormal",
                     "name":"是否考勤異常",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "abnormal":{
                     "id":"abnormal",
                     "name":"考勤異常數量",
                     "value":5,
                     "type":"integer",
                     "format":"count"
                  },
		  "photo":{
		     "id":"photo",
		     "name":"員工照片",
		     "value":"",
		     "type":"string",
		     "format":"base64"
		  },
                  "type":"object",
                  "format":"n/a"
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
            "count":"數量",
	    "base64":"Base64資料庫格式",
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
