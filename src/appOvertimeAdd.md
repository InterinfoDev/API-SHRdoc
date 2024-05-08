# appOvertimeAdd
新增實際加班單，新增事後加班單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeAdd
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
| request | {'empid':'9912011', 'overplanPno':'', 'startDate':'20220711', 'startTime':'2100', 'endTime':'2300', 'reason':'kevin中文實際加班單測試', 'payType':'B', 'overtimeDepartment':'9', 'allowanceClass':'', 'overtimeType':'A', 'totalPayHour':'2.0', 'totalRestHour':'0.0', 'newEatHour':'0.0', 'approvedProject':'000', 'oldEatHour':'0.0', 'isEat':true, 'beforeWork':false, 'naturalDisaster':false, 'earlyLeave':false, 'misAmt':'0', 'file':[{'fileName':'kevin.jpg','fileData':'xxx'}], 'confirmDialog':[{'confirmKey':'value'}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"9912011", 
      "overplanPno":"",
      "startDate":"20220711",
      "startTime":"2100",    
      "endTime":"2300",      
      "reason":"kevin中文實際加班單測試",   
      "overtimeType":"A",
      "overtimeDepartment":"9",
      "payType":"B",
      "allowanceClass":"",
      "totalPayHour":"2.0",
      "totalRestHour":"0.0",
      "newEatHour":"0.0",
      "oldEatHour":"0.0",
      "approvedProject":"222",
      "isEat":true,
      "earlyLeave":false,
      "naturalDisaster":false,
      "beforeWork":false,
      "misAmt":"0",
      "file":[{
        "fileName":"kevin.jpg",
        "fileData":"base64"
      }],
      "confirmDialog":[{
         "confirmKey":"value"
      }]
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
| overplanPno | xxx | String | 預定加班單號 | 實際加班單(Y)/事後加班單(N) | n/a |
| startDate | 20220527 | String | 起始日期 | Y | YYYYmmdd |
| startTime | 1900 | String | 起始時間 | Y | HHmm |  
| endTime | 2300 | String | 結束時間 | Y | HHmm |         
| reason | 20220524kevinOverplanTest | String | 加班內容 | Y | n/a |
| payType | A | String | 給付方式 | Y | n/a |
| allowanceClass |  | String | 津貼班別 | Y | n/a |
| overtimeDepartment | 9 | String | 加班部門 | Y | n/a |
| overtimeType | A | String | 加班類別 | Y | n/a |
| totalPayHour | 0.0 | String | 總計給薪時數 | Y | hour | 
| totalRestHour | 0.0 | String | 總計補休時數 | Y | hour |
| newEatHour | 0.0 | String | 新用餐時間 | Y | hour |
| oldEatHour | 0.0 | String | 原用餐時間 | Y | hour |
| approvedProject | 222 | String | 核准文號 | Y | n/a |
| isEat | false | boolean | 是否用餐 | Y | n/a | 
| beforeWork | false | boolean | 跨日往前加班 | Y | n/a | 
| naturalDisaster | false | boolean | 天災 | Y | n/a | 
| earlyLeave | false | boolean | 申請提早退勸 | Y | n/a | 
| misAmt | 0 | String | 誤餐費 | Y | currency | 
| file |  | String | 附件檔案 |  | n/a |
| fileName | test.jpg | String | 附件檔案 | N | n/a |
| fileData |  | String | 附件檔案 | N | base64 |
| confirmDialog |  | String | 提示視窗 |  | n/a |
| confirmKey | xxx | String | 提示訊息KEY值，後端會提供，若有提示視窗，confirmKey一定要給 | Y | n/a |
| value | xxx | String | 文字輸入或是下拉選項值，如果單純文字提醒value就放空白 | N | n/a |

### confirmType
| Category | Description |
|:----------|:------------|
| message | 單純提示訊息 |
| option | 有下拉選項 |
| text | 有文字輸入框 |

### Note
| 備註 |
|:----------|
| 呼叫完取得responce後，先判斷"isContinue"決定程式是否繼續執行，若"是"則代表有提示視窗，顯示提示視窗相關資訊，若"否"的話就看執行結果是否成功去顯示相對應資訊。當有提示視窗而使用者選擇buttonKey="N"的按鈕則程式中斷，選擇buttonKey="Y"的按鈕則需紀錄每次提示的KEY值並將下拉選項的值或文字輸入的內容回傳給後端，若單純為文字提醒，value放空白即可 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "n/a":""
         }
      },
      "addOvertime":{
         "name":"新增實際加班單",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"單據W002022062800003已進入簽核流程，謝謝",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
            },
            "confirmDialog":{ --kevin 新增提示視窗
               "name":"確認視窗",
               "type":"object",
               "value":{
                  "confirmKey":{
                     "name":"確認視窗鍵值",
                     "type":"string",
                     "value":"OVERLIMIT",
                     "format":"n/a",
                     "id":"confirmKey"
                  },
                  "confirmType":{
                     "name":"確認視窗種類",
                     "type":"string",
                     "value":"message",
                     "format":"n/a",
                     "id":"confirmType"
                  },
                  "confirmButton":{
                     "name":"確認視窗按鈕",
                     "type":"object",
                     "value":{
                        "confirm":{
                           "name":"確認",
                           "type":"object",
                           "value":{
                              "buttonKey":{
                                 "name":"按鈕代碼",
                                 "type":"string",
                                 "value":"Y",
                                 "format":"n/a",
                                 "id":"buttonId"
                              },
                              "buttonName":{
                                 "name":"按鈕名稱",
                                 "type":"string",
                                 "value":"是",
                                 "format":"n/a",
                                 "id":"buttonName"
                              },
                              "buttonVisible":{
                                 "name":"是否顯示",
                                 "type":"boolean",
                                 "value":true,
                                 "format":"n/a",
                                 "id":"visible"
                              }
                           },
                           "format":"n/a",
                           "id":"confirm"
                        },
                        "cancel":{
                           "name":"取消",
                           "type":"object",
                           "value":{
                              "buttonKey":{
                                 "name":"按鈕代碼",
                                 "type":"string",
                                 "value":"N",
                                 "format":"n/a",
                                 "id":"buttonId"
                              },
                              "buttonName":{
                                 "name":"按鈕名稱",
                                 "type":"string",
                                 "value":"否",
                                 "format":"n/a",
                                 "id":"buttonName"
                              },
                              "buttonVisible":{
                                 "name":"是否顯示",
                                 "type":"boolean",
                                 "value":true,
                                 "format":"n/a",
                                 "id":"visible"
                              }
                           },
                           "format":"n/a",
                           "id":"cancel"
                        }
                     },
                     "format":"n/a",
                     "id":"confirmButton"
                  },
                  "confirmTitle":{
                     "name":"確認視窗標題",
                     "type":"string",
                     "value":"警告",
                     "format":"n/a",
                     "id":"confirmTitle"
                  },
                  "confirmOption":{
                     "name":"確認視窗選項",
                     "type":"array",
                     "value":[
                        {   --測試資料
                           "optionId":{
                              "name":"選項代號",
                              "type":"string",
                              "value":"A",
                              "format":"n/a",
                              "id":"optionId"
                           },
                           "optionValue":{
                              "name":"選項名稱",
                              "type":"string",
                              "value":"補休",
                              "format":"n/a",
                              "id":"optionValue"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"confirmOption"
                  },
                  "confirmContent":{   --kevin 新增判斷程式是否繼續執行
                     "name":"確認視窗訊息",
                     "type":"string",
                     "value":"從連續排上班至總計天已超過天，是否繼續執行?",
                     "format":"n/a",
                     "id":"confirmContent"
                  }
               },
               "format":"n/a",
               "id":"confirmDialog"
            },
            "isContinue":{
               "name":"程式是否繼續執行",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"isContinue"
            }
         },
         "format":"n/a",
         "id":"addOvertime"
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
