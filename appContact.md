# appContact

取得夥伴查詢資料

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appContact
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
| request | {} | Object | 查詢條件


### JSON representation

Here is a JSON representation of request.

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
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


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "id":"contact",
         "name":"通訊錄功能",
         "value":[
            {
               "id":"departmentMember",
               "name":"技術處",
               "value":[
                  {
                     "id":"employeeInfo",
                     "name":"員工資訊",
                     "value":{
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
                        "depNumber":{
                           "id":"depNumber",
                           "name":"部門暗碼",
                           "value":2,
                           "type":"integer",
                           "format":"n/a"
                        },
                        "depCode":{
                           "id":"deoCode",
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
                        "empid":{
                           "id":"empid",
                           "name":"員工編號",
                           "value":"L100387",
                           "type":"string",
                           "format":"n/a"
                        },
                        "position":{
                           "id":"position",
                           "name":"職稱",
                           "value":"CTO",
                           "type":"string",
                           "format":"n/a"
                        },
                        "workPosition":{
                           "id":"workPosition",
                           "name":"職位",
                           "value":"技術長",
                           "type":"string",
                           "format":"n/a"
                        },
                        "photo":{
                           "id":"photo",
                           "name":"員工照片",
                           "value":"",
                           "type":"string",
                           "format":"base64"
                        },
                        "email":{
                           "id":"email",
                           "name":"電子郵件",
                           "value":"xxx@interinfo.com.tw",
                           "type":"string",
                           "format":"email"
                        },
                        "mobile":{
                           "id":"mobile",
                           "name":"行動電話",
                           "value":{
                              "nationalCode":{
                                 "id":"nationalCode",
                                 "name":"國碼",
                                 "value":"886",
                                 "type":"string",
                                 "format":"phone"
                              },
                              "telephone":{
                                 "id":"telephone",
                                 "name":"電話號碼",
                                 "value":"09123456789",
                                 "type":"string",
                                 "format":"phone"
                              }
                           },
                           "type":"object",
                           "format":"n/a"
                        },
                        "workplace":{
                           "id":"workplace",
                           "name":"工作地點",
                           "value":"台北",
                           "type":"string",
                           "format":"n/a"
                        },
                        "officePhone":{
                           "id":"officePhone",
                           "name":"辦公電話",
                           "value":{
                              "areaCode":{
                                 "id":"areaCode",
                                 "name":"區碼",
                                 "value":"02",
                                 "type":"string",
                                 "format":"phone"
                              },
                              "telephone":{
                                 "id":"telephone",
                                 "name":"電話號碼",
                                 "value":"82271675",
                                 "type":"string",
                                 "format":"phone"
                              },
                              "extension":{
                                 "id":"extension",
                                 "name":"分機號碼",
                                 "value":"600",
                                 "type":"string",
                                 "format":"n/a"
                              }
                           },
                           "type":"object",
                           "format":"n/a"
                        }
                     },
                     "type":"object",
                     "format":"n/a"
                  }
               ],
               "type":"array",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "phone":"電話號碼，可撥打",
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
