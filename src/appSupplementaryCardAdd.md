# appSupplementaryCardAdd
員工考勤補卡

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardAdd
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
| request | {"empid":"admin","cardType":"I","cardDate":"20220217","cardTime":"1857","reasonCode":"001","note":"忘記帶卡","file":[{"fileName":"test.jpg","fileData":"base64"}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin",
      "cardType":"I",
      "cardDate":"20220217",
      "cardTime":"1857",
      "reasonCode":"001",
      "note":"忘記帶卡",
      "file":[
         {
            "fileName":"test.jpg",
            "fileData":"base64"
         }
      ]
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| empid | admin | String | 員工編號 | Y | n/a | 異動欄位 |
| cardType | I/O | String | 補卡別 | Y | n/a | 進卡:I,出卡:O |
| cardDate | 20220217 | String | 補卡日期 | Y | n/a | AC(YYYYmmdd) |
| cardTime | 1857 | String | 補卡時間 | Y | n/a | TIME(HHmm) |
| reasonCode | 001 | String | 補卡原因代碼 | Y | n/a | 根據原因設定檔的代碼 |
| note | 忘記帶卡 | String | 備註 | Y | n/a | 補卡原因 |
| file |  | String | 附件檔案 |  | n/a | 補卡附件 |
| fileName | test.jpg | String | 附件檔案 | N | n/a | 補卡附件 |
| fileData |  | String | 附件檔案 | N | base64 | 補卡附件 |

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
      "supplementaryCardData":{
         "name":"新增補卡資料",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":false,
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
                     "value":"HOLIDAY_CHECK",
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
                     "value":"提醒",
                     "format":"n/a",
                     "id":"confirmTitle"
                  },
                  "confirmOption":{
                     "name":"確認視窗選項",
                     "type":"array",
                     "value":[
                        
                     ],
                     "format":"n/a",
                     "id":"confirmOption"
                  },
                  "confirmContent":{
                     "name":"確認視窗訊息",
                     "type":"string",
                     "value":"當日班別為例、休假 是否仍要繼續",
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
         "id":"supplementaryCardData"
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
