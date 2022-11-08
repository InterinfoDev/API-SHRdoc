# appMegaPhoneAdd
大聲公新增功能

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appMegaPhoneAdd
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
| request | {"empid":"admin","startDate":"20220629","line":"N","content":"TEST","sdept":"1","sempid":"admin","cpnyid":"TW"} | Object | 畫面上所有欄位資料

### JSON representation Case 1
Here is a JSON representation of request.
```json
{ 
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin", 
      "startDate":"20220629",
      "line":"N",    
      "content":"TEST",      
      "sdept":"1",        
      "sempid":"admin",          
      "cpnyid":"TW"
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
| startDate | 20220629 | String | 發布日期 | Y | YYYYmmdd |
| line | N | String | LINE通知 | Y | HHmm |  
| content | TEST | String | 內容說明 | Y | n/a  |         
| sdept | 1 | String | 發佈單位 | N | n/a |
| sempid | admin | String | 發佈者 | Y | n/a |
| cpnyid | TW | admin | 公司別 | Y | n/a  | 

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "appMegaphone":{
         "name":"新增大聲公",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"異動成功",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
            }
         },
         "format":"n/a",
         "id":"appMegaphone"
      },
      "properties":{
         "format":{
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
