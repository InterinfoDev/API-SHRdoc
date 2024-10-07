# appLogin
驗證使用者帳號密碼

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appLogin
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {uid:admin,pwd:1234,deviceBindId:test,deviceType:ios} | Object | 請將帳號密碼組成物件 |

### JSON representation
Here is a JSON representation of request.
```json
{
  "request":{
      "uid":"admin",
      "pwd":"1234",
      "deviceBindId":"test",
      "deviceType":"ios"
  }
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| request | Object | 要求本文 |

### tabBarControllerTthirdFunction
| FunctionCode | FunctionName |
|:---------|:------------|
| 1 | 鈴鐺 |
| 2 | 大聲公 |
| 3 | 噠噠 |

### bellType
| FunctionCode | FunctionName |
|:---------|:------------|
| 1 | 紅點 |
| 2 | NEW |

### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| uid | admin | String | 登入帳號 | Y | n/a |
| pwd | 1234 | String | 登入密碼 | Y | n/a |
| deviceBindId | test | String | 綁定id | Y | n/a |
| deviceType | ios | String | 裝置類型 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "登入成功"
   ],
   "data":{
      "loginState":{
         "name":"登入狀態",
         "type":"object",
         "value":{
            "resultType":{
               "name":"回傳結果",
               "type":"string",
               "value":"success",
               "format":"n/a",
               "id":"resultType"
            }
         },
         "format":"n/a",
         "id":"loginState"
      },
      "employee":{
         "name":"個人資訊",
         "type":"object",
         "value":{
            "isBinding":{
               "name":"是否已被綁定",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"isBinding"
            },
            "useBinding":{
               "name":"是否開啟綁定功能",
               "type":"boolean",
               "value":false,
               "format":"n/a",
               "id":"useBinding"
            },
            "empid":{
               "name":"員工編號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"empid"
            },
            "companySimpleName":{
               "name":"公司簡稱",
               "type":"string",
               "value":"英特內",
               "format":"n/a",
               "id":"companySimpleName"
            },
            "depNumber":{
               "name":"部門暗碼",
               "type":"integer",
               "value":1,
               "format":"n/a",
               "id":"depNumber"
            },
            "bindingConfig":{
               "name":"裝置綁定機制設定",
               "type":"integer",
               "value":3,
               "format":"n/a",
               "id":"bindingConfig"
            },
            "empFullName":{
               "name":"員工姓名",
               "type":"string",
               "value":"AOO",
               "format":"n/a",
               "id":"empFullName"
            },
            "depFullName":{
               "name":"部門名稱",
               "type":"string",
               "value":"台北總公司",
               "format":"n/a",
               "id":"depFullName"
            },
            "companyId":{
               "name":"公司代號",
               "type":"string",
               "value":"1",
               "format":"n/a",
               "id":"companyId"
            },
            "empFullEname":{
               "name":"員工英文姓名",
               "type":"string",
               "value":"TESOO",
               "format":"n/a",
               "id":"empFullEname"
            },
            "depCode":{
               "name":"部門代號",
               "type":"string",
               "value":"1",
               "format":"n/a",
               "id":"depCode"
            }
         },
         "format":"n/a",
         "id":"employee"
      },
      "properties":{
         "n/a":""
      },
      "uid":"98599308101484732326",
      "right":"5134191190417354337727876278364154894157386843084143654173589798053183478405081380635",
      "type":"object",
      "system":{
         "name":"系統參數",
         "type":"object",
         "value":{
            "bellType":{
               "name":"鈴鐺預設新通知樣式",
               "type":"string",
               "value":"2",
               "format":"n/a",
               "id":"bellType"
            },
            "tabBarControllerThirdFunction":{
               "name":"Tab Bar Controller 第三項功能",
               "type":"string",
               "value":"3",
               "format":"n/a",
               "id":"tabBarControllerThirdFunction"
            },
            "azureIP":{
               "name":"雲端IP",
               "type":"string",
               "value":"https://www.interinfo.com.tw",
               "format":"n/a",
               "id":"azureIP"
            }
         },
         "format":"n/a",
         "id":"system"
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

### HTTP Response when Failed (Account Locked)
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

### HTTP Response when Failed (Password Expired)
判斷密碼到期變更設定
```json
{
   "Response":{
      "status":"fail",
      "code":500,
      "message":[
         "您的密碼因已到期無法登入，請至電腦版進行變更再操作"
      ],
      "data":{
         "loginState":{
            "name":"登入狀態",
            "type":"object",
            "value":{
               "resultType":{
                  "name":"回傳結果",
                  "type":"string",
                  "value":"passwordExpired",
                  "format":"n/a",
                  "id":"resultType"
               }
            },
            "format":"n/a",
            "id":"loginState"
         }
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
