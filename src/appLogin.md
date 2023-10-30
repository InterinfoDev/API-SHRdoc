# appLogin
驗證使用者帳號密碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appLogin
```

### HTTP Request Mehod
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {uid:admin,pwd:1234} | Object | 請將帳號密碼組成物件 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "request":{
      "uid":"admin",
      "pwd":"1234"
  }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| request | Object | 要求本文 |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| uid | admin | String | 登入帳號 | Y | n/a |
| pwd | 1234 | String | 登入密碼 | Y | n/a |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "登入成功"
    ],
    "data": {
        "loginState": {
            "name": "登入狀態",
            "type": "object",
            "value": {
                "resultType": {
                    "name": "回傳結果",
                    "type": "string",
                    "value": "success",
                    "format": "n/a",
                    "id": "resultType"
                }
            },
            "format": "n/a",
            "id": "loginState"
        },
        "employee": {
            "name": "個人資訊",
            "type": "object",
            "value": {
                "depCode": {
                    "name": "部門代號",
                    "type": "string",
                    "value": "99999",
                    "format": "n/a",
                    "id": "depCode"
                },
                "companyId": {
                    "name": "公司代號",
                    "type": "string",
                    "value": "TW",
                    "format": "n/a",
                    "id": "companyId"
                },
                "companySimpleName": {
                    "name": "公司簡稱",
                    "type": "string",
                    "value": "72英特內(中和)",
                    "format": "n/a",
                    "id": "companySimpleName"
                },
                "depNumber": {
                    "name": "部門暗碼",
                    "type": "integer",
                    "value": 1,
                    "format": "n/a",
                    "id": "depNumber"
                },
                "empFullName": {
                    "name": "員工姓名",
                    "type": "string",
                    "value": "系統管理員",
                    "format": "n/a",
                    "id": "empFullName"
                },
                "empid": {
                    "name": "員工編號",
                    "type": "string",
                    "value": "admin",
                    "format": "n/a",
                    "id": "empid"
                },
                "depFullName": {
                    "name": "部門名稱",
                    "type": "string",
                    "value": "英特內股份有限公司",
                    "format": "n/a",
                    "id": "depFullName"
                },
                "empFullEname": {
                    "name": "員工英文姓名",
                    "type": "string",
                    "value": "Administrator",
                    "format": "n/a",
                    "id": "empFullEname"
                }
            },
            "format": "n/a",
            "id": "employee"
        },
        "properties": {
            "n/a": ""
        },
        "uid": "98599308101484732326",
        "right": "513419119041735433367561625448648202801232182995256636587932016607439201462466556235182663080673828674556200385271466125559349357786197118252096238747191633938599840684449342490964011524427764799493328110221539965006552590466959002677036856863519908176241437809573716163508936719855927717064013479997584572837246619648420374378288189675965452573416450376175273412420409191239097059629612395701880365980754522949348194952849418106023010387607494224029080312442356345333827742668253005042661612460080367422756341547727876278364154894157386843084143654173589798053183478405081380635",
        "type": "object",
        "system": {
            "name": "系統參數",
            "type": "object",
            "value": {
                "haveDada": {
                    "name": "是否有噠噠功能",
                    "type": "boolean",
                    "value": true,
                    "format": "n/a",
                    "id": "haveDada"
                },
                "tabBarControllerTthirdFunction": {
                    "name": "Tab Bar Controller 第三項功能",
                    "type": "string",
                    "value": "3",
                    "format": "n/a",
                    "id": "tabBarControllerTthirdFunction"
                },
                "azureFile": {
                    "name": "雲端PKG檔",
                    "type": "string",
                    "value": "hrm8w.pkg",
                    "format": "n/a",
                    "id": "azureFile"
                },
                "azureIP": {
                    "name": "雲端IP",
                    "type": "string",
                    "value": "http://59.124.100.151:8090",
                    "format": "n/a",
                    "id": "azureIP"
                }
            },
            "format": "n/a",
            "id": "system"
        }
    }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料，除非驗證失敗
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
   "status":"fail",
   "code":500,
   "message":[
      "登入失敗已超過1次，帳號已鎖定 , 請洽 HR 人員! Failed to login , cause your account has been locked , please contact system manager."
   ],
   "data":{
      "loginState":{
         "name":"登入狀態",
         "type":"object",
         "value":{
            "resultType":{
               "name":"回傳結果",
               "type":"string",
               "value":"locked",
               "format":"n/a",
               "id":"resultType"
            }
         },
         "format":"n/a",
         "id":"loginState"
      }
   }
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
