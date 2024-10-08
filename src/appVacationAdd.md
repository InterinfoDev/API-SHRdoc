# appVacationAdd
員工請假

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationAdd
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
| request | {'empid':'admin', 'vacationCode':'000', 'startDate':'20220429', 'endDate':'20220429', 'startTime':'0830', 'endTime':'1700', 'reason':'kevin中文測試', 'delayReason':'', 'place':'', 'vacationType':'','outsideId':'', 'familyName':'','jobAgent':'10900015', 'specialDate':'', 'isHoliday':false, 'planeTicket':0, 'flowAgent':'10900015', 'flowAgent1':'10900015', 'flowAgent2':'10900015', 'flowAgent3':'10900015', 'file':[{'fileName':'kevin.jpg','fileData':'base64'}], 'confirmDialog':[{'confirmKey':'value'}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin", 
      "vacationCode":"000",
      "startDate":"20220429",  
      "endDate":"20220429",   
      "startTime":"0830",    
      "endTime":"1700",    
      "reason":"kevin中文測試",
      "delayReason":"",
      "jobAgent":"10900015",
      "specialDate":"",
      "isHoliday":false,
      "planeTicket":0,
      "specialDate":"",
      "place":"",
      "vacationType":"",
      "outsideId":"",
      "familyName":"",
      "flowAgent":"10900015",
      "flowAgent1":"10900015",   
      "flowAgent2":"10900015",   
      "flowAgent3":"10900015",  
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
| vacationCode | 000 | String | 假別代碼 | Y | n/a |
| startDate | 20220429 | String | 起始日期 | Y | YYYYmmdd |
| endDate | 20220429 | String | 結束日期 | Y | YYYYmmdd |
| startTime | 0830 | String | 起始時間 | Y | HHmm |
| endTime | 1700 | String | 結束時間 | Y | HHmm |
| reason | kevin中文測試 | String | 請假說明 | Y | n/a |
| delayReason |  | String | 逾時請假說明 | N | n/a |
| jobAgent | 10900015 | String | 職務代理人 | N | n/a | 
| specialDate |  | String | 特殊日期 | N | YYYYmmdd |
| isHoliday | false | boolean | 是否包含假日 | N | n/a |
| planeTicket | 0 | integer | 機票 | N | ticket |
| place |  | String | 地點 | N | ticket |
| vacationType |  | String | 請假類別 | N | ticket |
| outSideId |  | String | 相關單號 | N | ticket |
| familyName |  | String | 親屬姓名 | N | ticket |
| flowAgent | 10900015 | String | 簽核代理人 | N | n/a | 
| flowAgent1 | 10900015 | String | 代理人一 | N | n/a | 
| flowAgent2 | 10900015 | String | 代理人二 | N | n/a | 
| flowAgent3 | 10900015 | String | 代理人三 | N | n/a | 
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
      "addVacation":{
         "name":"新增請假單",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"單據W00202204290004已進入簽核流程，謝謝",
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
         "id":"addVacation"
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
