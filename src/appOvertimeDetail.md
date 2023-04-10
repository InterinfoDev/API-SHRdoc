# appOvertimeDetail
查詢該假單詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeDetail
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
| request | {pno:H002022031100002, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的假單單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "pno":"H002022031100002",  
        "empid":"admin"
    }
}
```

### Properties
| Property | Type | Description | 
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### fieldType
| Type | Description | key |
|:---------|:------------|:------------|
| text | 文字顯示類型  | fieldValue |
| file | 附件下載顯示類型 | files |
| switch | 開關類型 | switch |


### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| pno | W00202201250001 | String | 單據編號 | Y | n/a |
| empid | admin | String | 員工編號 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "holidayRateDetail":{
         "name":"假日加班倍率時數",
         "type":"object",
         "value":[
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"holidayRate1",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "8.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.00",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"holidayRate2",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.34",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"holidayRate3",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.34",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"holidayRate4",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.67",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            }
         ],
         "format":"n/a",
         "id":"holidayRateDetail"
      },
      "flowHistory": {
            "name": "流程紀錄",
            "type": "object",
            "value": {
                "historyKey": {
                    "name": "流程鍵值",
                    "type": "string",
                    "value": "4018143326273716525552090972897090755341893430474685977954583012953934710584411029083038347111586025145545203390274432940930977559895422",
                    "format": "n/a",
                    "id": "historyKey"
                }
            },
            "format": "n/a",
            "id": "flowHistory"
      },
      "overtimeDetail":{
         "name":"實際加班單詳細資訊",
         "type":"object",
         "value":[
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"pno",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "H002022031100002"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"單據編號",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"overplanPno",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        ""
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"預定加班單號",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"companyFullName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "72英特內全名(中和)"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"公司別",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"empFullName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "系統管理員"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"員工姓名",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"empFullEname",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "Administrator"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"員工英文名字",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"depFullName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "L1線B班"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"現職部門",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"overtimeDepFullName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "L1線B班"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"加班部門",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"overtimeType",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "一般加班"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"加班種類",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"allowanceClass",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        ""
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"津貼班別",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
                "name": "欄位資訊",
                "type": "object",
                "value": {
                    "fieldType": {
                        "name": "欄位類型",
                        "type": "string",
                        "value": "text",
                        "format": "n/a",
                        "id": "fieldType"
                    },
                    "fieldId": {
                        "name": "欄位代號",
                        "type": "string",
                        "value": "oldPayTypeName",
                        "format": "n/a",
                        "id": "fieldId"
                    },
                    "fieldValue": {
                        "name": "欄位資料",
                        "type": "array",
                        "value": [
                            ""
                        ],
                        "format": "n/a",
                        "id": "fieldValue"
                    },
                    "fieldName": {
                        "name": "欄位名稱",
                        "type": "string",
                        "value": "原給付方式",
                        "format": "n/a",
                        "id": "fieldName"
                    }
                },
                "format": "n/a",
                "id": "field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"payTypeName",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "給薪"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"給付方式",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"overtimeStartTime",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "2022/01/01 08:00"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"起始時間",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"overtimeEndTime",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "2022/01/01 16:00"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"結束時間",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"amt",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "8.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"總計時數",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"switch",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"naturalDisaster",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "switch":{
                     "name":"開關",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"switch"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"天災",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"switch",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"earlyLeave",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "switch":{
                     "name":"開關",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"switch"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"申請提早退勤(加班時數=實際出勤時數)",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"switch",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"isEat",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "switch":{
                     "name":"開關",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"switch"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"是否用餐",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"newEatAmt",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"新用餐時間",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"oldEatAmt",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"原用餐時間",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"totalPaidAmt",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "8.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"總計給薪時數",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
                "name": "欄位資訊",
                "type": "object",
                "value": {
                    "fieldType": {
                        "name": "欄位類型",
                        "type": "string",
                        "value": "text",
                        "format": "n/a",
                        "id": "fieldType"
                    },
                    "fieldId": {
                        "name": "欄位代號",
                        "type": "string",
                        "value": "oldTotalRestAmt",
                        "format": "n/a",
                        "id": "fieldId"
                    },
                    "fieldValue": {
                        "name": "欄位資料",
                        "type": "array",
                        "value": [
                            "A"
                        ],
                        "format": "hour",
                        "id": "fieldValue"
                    },
                    "fieldName": {
                        "name": "欄位名稱",
                        "type": "string",
                        "value": "原補休時數",
                        "format": "n/a",
                        "id": "fieldName"
                    }
                },
                "format": "n/a",
                "id": "field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"totalRestAmt",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"總計補休時數",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
                "name": "欄位資訊",
                "type": "object",
                "value": {
                    "fieldType": {
                        "name": "欄位類型",
                        "type": "string",
                        "value": "text",
                        "format": "n/a",
                        "id": "fieldType"
                    },
                    "fieldId": {
                        "name": "欄位代號",
                        "type": "string",
                        "value": "misAmt",
                        "format": "n/a",
                        "id": "fieldId"
                    },
                    "fieldValue": {
                        "name": "欄位資料",
                        "type": "array",
                        "value": [
                            "0"
                        ],
                        "format": "currency",
                        "id": "fieldValue"
                    },
                    "fieldName": {
                        "name": "欄位名稱",
                        "type": "string",
                        "value": "誤餐費金額",
                        "format": "n/a",
                        "id": "fieldName"
                    }
                },
                "format": "n/a",
                "id": "field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"apprdate",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "20220101"
                     ],
                     "format":"YYYYmmdd",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"入帳日期",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"note",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "aa"
                     ],
                     "format":"n/a",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"詳細資料",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"switch",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"beforeWork",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "switch":{
                     "name":"開關",
                     "type":"boolean",
                     "value":false,
                     "format":"n/a",
                     "id":"switch"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"跨日往前加班",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"file",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"uploadFiles",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "files":{
                     "name":"附件資訊",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"files"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"附件",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            }
         ],
         "format":"n/a",
         "id":"overtimeDetail"
      },
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "hour":"小時",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "dailyRateDetail":{
         "name":"平日加班倍率時數",
         "type":"object",
         "value":[
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"dailyRate1",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"0.00",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"dailyRate2",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.34",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"dailyRate3",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.67000",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            },
            {
               "name":"欄位資訊",
               "type":"object",
               "value":{
                  "fieldType":{
                     "name":"欄位類型",
                     "type":"string",
                     "value":"text",
                     "format":"n/a",
                     "id":"fieldType"
                  },
                  "fieldId":{
                     "name":"欄位代號",
                     "type":"string",
                     "value":"dailyRate4",
                     "format":"n/a",
                     "id":"fieldId"
                  },
                  "fieldValue":{
                     "name":"欄位資料",
                     "type":"array",
                     "value":[
                        "0.00"
                     ],
                     "format":"hour",
                     "id":"fieldValue"
                  },
                  "fieldName":{
                     "name":"欄位名稱",
                     "type":"string",
                     "value":"1.6700",
                     "format":"n/a",
                     "id":"fieldName"
                  }
               },
               "format":"n/a",
               "id":"field"
            }
         ],
         "format":"n/a",
         "id":"dailyRateDetail"
      }
   }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
