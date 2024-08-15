# appVacationVerifyField
請假畫面欄位檢核，之後若其他功能有需要用到欄位檢核也會依照此格式回傳，主要會傳入欲檢核的欄位名稱以及畫面上所有欄位的資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationVerifyField
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
| request | {'fieldName':'vacationType', 'empid':'admin', 'vacationCode':'05', 'startDate':'20240808', 'endDate':'20240808', 'startTime':'0900', 'endTime':'1800', 'reason':'kevin中文測試', 'delayReason':'', 'jobAgent':'', 'specialDate':'20240506', 'isHoliday':false, 'planeTicket':0, 'flowAgent':'', 'firstFile':'', 'vacationType':'2'} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "fieldName":"vacationType",
   "empid":"admin",
   "vacationCode":"05",
   "startDate":"20240808",
   "endDate":"20240808",
   "startTime":"0900",
   "endTime":"1800",
   "reason":"kevin中文測試",
   "delayReason":"",
   "jobAgent":"",
   "specialDate":"20240506",
   "isHoliday":false,
   "planeTicket":0,
   "flowAgent":"",
   "firstFile":"",
   "vacationType":"2"
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
| fieldName | vacationStartDate | String | 欄位名稱 | Y | n/a |
| empid | admin | String | 員工編號 | N | n/a |
| vacationCode | 000 | String | 假別代碼 | N | n/a |
| startDate | 20220503 | String | 起始日期 | N | YYYYmmdd |
| endDate | 20220503 | String | 結束日期 | N | YYYYmmdd |    
| startTime | 0830 | String | 起始時間 | N | HHmm |  
| endTime | 1730 | String | 結束時間 | N | HHmm |         
| reason | kevin中文測試 | String | 請假說明 | N | n/a |
| delayReason |  | String | 逾時請假說明 | N | n/a |
| jobAgent | 10900015 | String | 職務代理人 | N | n/a | 
| specialDate |  | String | 特殊日期 | N | YYYYmmdd |
| isHoliday | false | boolean | 是否包含假日 | N | n/a |
| planeTicket | 0 | integer | 機票 | N | ticket |
| flowAgent | 10900015 | String | 簽核代理人 | N | n/a | 
| flowAgent1 | 10900015 | String | 代理人一 | N | n/a | 
| flowAgent2 | 10900015 | String | 代理人二 | N | n/a | 
| flowAgent3 | 10900015 | String | 代理人三 | N | n/a | 
| file |  | String | 附件檔案 |  | n/a |
| fileName | test.jpg | String | 附件檔案 | N | n/a |
| fileData |  | String | 附件檔案 | N | base64 |
| vacationType | 2 | String | 請假類別 | N | n/a |

### Using Field
| FieldName | Description |
|:---------|:-----|
| startDate | 起始日期 |
| specialDate | 特殊日期(20221007新增) |

### HTTP Response when Successful
```json
{
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "verifyResult": {
      "name": "檢核結果",
      "type": "object",
      "value": {
        "actions": {
          "name": "異動欄位",
          "type": "object",
          "value": {
            "setEditable": {
              "name": "設定欄位可否編輯",
              "type": "array",
              "value": [
                {
                  "name": "相關單號",
                  "type": "boolean",
                  "value": true,
                  "format": "n/a",
                  "id": "outSideId"
                }
              ],
              "format": "n/a",
              "id": "setEditable"
            },
            "setValue": {
              "name": "設定欄位值",
              "type": "array",
              "value": [
                {
                  "name": "相關單號",
                  "type": "string",
                  "value": "",
                  "format": "n/a",
                  "id": "outSideId"
                }
              ],
              "format": "n/a",
              "id": "setValue"
            },
            "setVisible": {
              "name": "設定欄位是否顯示",
              "type": "array",
              "value": [
                {
                  "name": "相關單號",
                  "type": "boolean",
                  "value": true,
                  "format": "n/a",
                  "id": "outSideId"
                }
              ],
              "format": "n/a",
              "id": "setVisible"
            }
          },
          "format": "n/a",
          "id": "actions"
        }
      },
      "format": "n/a",
      "id": "verifyResult"
    },
    "properties": {
      "format": {
        "HHmm": "時間時分",
        "YYYYmmdd": "西元年月日",
        "n/a": ""
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
