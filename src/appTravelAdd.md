# appTravelAdd
員工出差

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelAdd
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
| request | {'empid':'admin','startDate':'20220628','endDate':'20220630','startTime':'1230','endTime':'1830','note':'AndyHou測試出差單備註','jobAgent':'0169','flowAgent':'0169','flowAgent1':'','flowAgent2':'','flowAgent3':'',"travelType":"A",'travelPlace':'台北南港','traffic':'4','contact':'測試-聯絡方式','currency':'USD','isHoliday':false,'people':'測試-出差人員及分工方式','visit':'測試-拜訪對象','schedule':'測試-行程規劃','point':'測試-訪談重點及預期效果','authorize':'測試-希望授權事項及幅度','assist':'測試-協助他部門辦理事項','preCost':300.0,'scheduleList':[{'startDate':'20220628','endDate':'20220630','days':'3','city':'台北'}],'scheduleFile':[{'fileName':'測試檔案.jpg','fileData':''}],'travelFile':[{'fileName':'測試檔案.jpg','fileData':''}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "addTravel": {
      "name": "新增出差單",
      "type": "object",
      "value": {
        "executeMessage": {
          "name": "異動訊息",
          "type": "string",
          "value": "本單(xxx)已完成確認，謝謝",
          "format": "n/a",
          "id": "executeMessage"
        },
        "executeResult": {
          "name": "異動結果",
          "type": "boolean",
          "value": true,
          "format": "n/a",
          "id": "executeResult"
        },
        "confirmDialog": {
          "name": "確認視窗",
          "type": "object",
          "value": {
            "confirmKey": {
              "name": "確認視窗鍵值",
              "type": "string",
              "value": "OVERLIMIT",
              "format": "n/a",
              "id": "confirmKey"
            },
            "confirmType": {
              "name": "確認視窗種類",
              "type": "string",
              "value": "message",
              "format": "n/a",
              "id": "confirmType"
            },
            "confirmButton": {
              "name": "確認視窗按鈕",
              "type": "object",
              "value": {
                "confirm": {
                  "name": "確認",
                  "type": "object",
                  "value": {
                    "buttonKey": {
                      "name": "按鈕代碼",
                      "type": "string",
                      "value": "Y",
                      "format": "n/a",
                      "id": "buttonId"
                    },
                    "buttonName": {
                      "name": "按鈕名稱",
                      "type": "string",
                      "value": "是",
                      "format": "n/a",
                      "id": "buttonName"
                    },
                    "buttonVisible": {
                      "name": "是否顯示",
                      "type": "boolean",
                      "value": true,
                      "format": "n/a",
                      "id": "visible"
                    }
                  },
                  "format": "n/a",
                  "id": "confirm"
                },
                "cancel": {
                  "name": "取消",
                  "type": "object",
                  "value": {
                    "buttonKey": {
                      "name": "按鈕代碼",
                      "type": "string",
                      "value": "N",
                      "format": "n/a",
                      "id": "buttonId"
                    },
                    "buttonName": {
                      "name": "按鈕名稱",
                      "type": "string",
                      "value": "否",
                      "format": "n/a",
                      "id": "buttonName"
                    },
                    "buttonVisible": {
                      "name": "是否顯示",
                      "type": "boolean",
                      "value": true,
                      "format": "n/a",
                      "id": "visible"
                    }
                  },
                  "format": "n/a",
                  "id": "cancel"
                }
              },
              "format": "n/a",
              "id": "confirmButton"
            },
            "confirmTitle": {
              "name": "確認視窗標題",
              "type": "string",
              "value": "警告",
              "format": "n/a",
              "id": "confirmTitle"
            },
            "confirmOption": {   --測試資料
              "name": "確認視窗選項",
              "type": "array",
              "value": [
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "A",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "A選項",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                }
              ],
              "format": "n/a",
              "id": "confirmOption"
            },
            "confirmContent": {
              "name": "確認視窗訊息",
              "type": "string",
              "value": "提醒您此區間已申請過請假(單號xxx)",
              "format": "n/a",
              "id": "confirmContent"
            }
          },
          "format": "n/a",
          "id": "confirmDialog"
        },
        "isContinue": {
          "name": "程式是否繼續執行",
          "type": "boolean",
          "value": true,
          "format": "n/a",
          "id": "isContinue"
        }
      },
      "format": "n/a",
      "id": "addTravel"
    },
    "properties": {
      "format": {
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
