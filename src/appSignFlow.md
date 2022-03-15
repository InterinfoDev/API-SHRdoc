# appSignFlow
取得簽核畫面核准或退簽按鈕所回傳的資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSignFlow
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
| request | {key:xxx, buttonKey:xxx, memo:xxx, uniqueKey[[uniqueField:xxx, uniqueValue:xxx]]} | Object | key,buttonKey,uniqueKey都由appFlowList取得

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "key":"635144642219404571194688689683105522531368129784502001284860188282814076207411", 
        "buttonKey":"[退簽]", 
        "memo":"kevin退簽測試", 
        "uniqueKey":[[{"uniqueField":"102466946499809093666", "uniqueValue":"20130402003"}]]
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
| key | 635144642219404571194688689683105522531368129784502001284860188282814076207411 | String | 鍵值 | Y | n/a |
| buttonKey | [退簽] | String | 按鈕代碼 | Y | n/a |
| memo | kevin退簽測試 | String | 簽核意見 | N(退簽時為Y) | n/a |
| uniqueKey | [{"uniqueField":"102466946499809093666", "uniqueValue":"20130402003"}] | Vector | 單據鍵值 | Y | n/a |
| uniqueField | 102466946499809093666 | String | 鍵值資料 | Y | n/a |
| uniqueValue | 20130402003 | String | 鍵值名稱 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "您已成功退簽1筆單據"
   ],
   "data":{
      "signCount":{
         "name":"簽核筆數",
         "type":"integer",
         "value":1,
         "format":"count",
         "id":"signCount"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "count":"數量",
            "n/a":"",
            "HHmmss":"時間時分秒"
         }
      },
      "approveTime":{
         "name":"簽核時間",
         "type":"string",
         "value":"093712",
         "format":"HHmmss",
         "id":"approveTime"
      },
      "approver":{
         "name":"簽核人員",
         "type":"string",
         "value":"admin",
         "format":"n/a",
         "id":"approver"
      },
      "approveDate":{
         "name":"簽核日期",
         "type":"string",
         "value":"20220315",
         "format":"YYYYmmdd",
         "id":"approveDate"
      }
   }
}
```

### HTTP Response when No Data 
```json
{
   "status":"fail",
   "code":500,
   "message":[
      "查無簽核資料"
   ],
   "data":{}
}
```

### HTTP Response when Failed
```json
{
   "status":"fail",
   "code":500,
   "message":[
      "XXX"
   ],
   "data":{}
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
