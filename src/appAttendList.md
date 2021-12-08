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
| request | {depNumber:[1], attendYM:202104, empid:[admin], companyId:97090920} | Object | 查詢條件(depNumber/companyId/empid至少選一輸入)

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "attendYM":"202104", 
        "companyId":"97090920",
        "depNumber":[1], --lucas 改成陣列 改名 depNumber，並改用integer
        "empid":["admin"] --lucas 改成陣列
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
| attendYM | 202104 | String | 查詢年月 | Y | AC(YYYYmm) |
| companyId | 97090920 | String | 公司代號 | N | n/a |
| depNumber | [1] | Array<Integer> | 部門代號 | N | n/a |
| empid | [admin] | Array<String> | 員工編號 | N | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{  --lucas 修改為main
         "id":"main",  --lucas 修改為main
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
                  "empFullName":{--lucas
                     "id":"empFullName",--lucas
                     "name":"員工中文姓名",
                     "value":"林奇杰",
                     "type":"string",
                     "format":"n/a"
                  },
                  "empFullEnName":{ --lucas
                     "id":"empFullEnName",--lucas
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
                  "depFullName":{	--lucas
                     "id":"depFullName", --lucas
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
		     "value":"base64",--lucas
		     "type":"string",
		     "format":"base64"
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
            "count":"數量",
	    "base64":"Base64資料庫格式",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
