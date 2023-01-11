# appOverplanAdd
新增預定加班單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOverplanAdd
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
| request | {{'empid':'admin', 'startDate':'20220527', 'startTime':'1900', 'endTime':'2200', 'reason':'xxx', 'payType':'A', 'totalPayHour':0.0, 'totalRestHour':0.0, 'specifyHour':0.0, 'oldEatHour':0.0, 'isEat':false, 'beforeWork':false, 'file':[{'fileName':'kevin.jpg','fileData':'base64'}], 'confirmDialog':[{'confirmKey':'value'}]} | Object | 畫面上所有欄位資料

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin", 
      "startDate":"20220527",
      "startTime":"1900",    
      "endTime":"2200",      
      "reason":"20220524kevinOverplanTest",        
      "payType":"A",          
      "totalPayHour":0.0,
      "totalRestHour":0.0,
      "specifyHour":0.0,
      "oldEatHour":0.0,
      "isEat":false,
      "beforeWork":false,
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
| startDate | 20220527 | String | 起始日期 | Y | YYYYmmdd |
| startTime | 1900 | String | 起始時間 | Y | HHmm |  
| endTime | 2300 | String | 結束時間 | Y | HHmm |         
| reason | 20220524kevinOverplanTest | String | 請假說明 | N | n/a |
| payType | A | String | 給付方式 | Y | n/a |
| totalPayHour | 0.0 | Decimal | 總計給薪時數 | Y | hour | 
| totalRestHour | 0.0 | Decimal | 總計補休時數 | Y | hour |
| specifyHour | 0.0 | Decimal | 指定用餐時間 | Y | hour |
| oldEatHour | 0.0 | Decimal | 原用餐時間 | Y | hour |
| isEat | false | boolean | 是否用餐 | Y | n/a | 
| beforeWork | false | boolean | 跨日往前加班 | Y | n/a | 
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
      "addOverplan":{
         "name":"新增預定加班單",
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
            "confirmDialog":{
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
                  "confirmContent":{
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
         "id":"addOverplan"
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
