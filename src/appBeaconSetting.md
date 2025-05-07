# appBeaconSetting
取得Beacon打卡資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBeaconSetting
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
| request | {} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
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


### HTTP Response when Successful
```json
{
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "beacon": {
      "name": "beacon",
      "type": "array",
      "value": [
        {
          "name": "beacon資訊",
          "type": "object",
          "value": {
            "place": {
              "name": "beacon設定位置",
              "type": "string",
              "value": "雲林",
              "format": "n/a",
              "id": "place"
            },
            "beaconMajor": {
              "name": "主要",
              "type": "integer",
              "value": 1,
              "format": "n/a",
              "id": "beaconMajor"
            },
            "beaconName": {
              "name": "beacon名稱",
              "type": "string",
              "value": "beacon test",
              "format": "n/a",
              "id": "beaconName"
            },
            "beaconMinor": {
              "name": "次要",
              "type": "integer",
              "value": 21356,
              "format": "n/a",
              "id": "beaconMinor"
            },
            "beaconUuid": {
              "name": "beacon代碼",
              "type": "string",
              "value": "B5B182C7-EAB1-4988-AA99-B5C1517008D7",
              "format": "n/a",
              "id": "beaconUuid"
            }
          },
          "format": "n/a",
          "id": "beaconInfo"
        },
        {
          "name": "beacon資訊",
          "type": "object",
          "value": {
            "place": {
              "name": "beacon設定位置",
              "type": "string",
              "value": "台北",
              "format": "n/a",
              "id": "place"
            },
            "beaconMajor": {
              "name": "主要",
              "type": "integer",
              "value": 1,
              "format": "n/a",
              "id": "beaconMajor"
            },
            "beaconName": {
              "name": "beacon名稱",
              "type": "string",
              "value": "beacon 測試",
              "format": "n/a",
              "id": "beaconName"
            },
            "beaconMinor": {
              "name": "次要",
              "type": "integer",
              "value": 21356,
              "format": "n/a",
              "id": "beaconMinor"
            },
            "beaconUuid": {
              "name": "beacon代碼",
              "type": "string",
              "value": "A1A182C7-EAB1-4988-AA99-B5C1517006E1",
              "format": "n/a",
              "id": "beaconUuid"
            }
          },
          "format": "n/a",
          "id": "beaconInfo"
        }
      ],
      "format": "n/a",
      "id": "beacon"
    },
    "button": {
      "name": "打卡按鈕資訊",
      "type": "array",
      "value": [
        {
          "name": "打卡按鈕資訊",
          "type": "object",
          "value": {
            "buttonKey": {
              "name": "按鈕鍵值",
              "type": "string",
              "value": "99924066065569631271",
              "format": "n/a",
              "id": "buttonKey"
            },
            "buttonName": {
              "name": "按鈕名稱",
              "type": "string",
              "value": "打卡",
              "format": "n/a",
              "id": "buttonName"
            }
          },
          "format": "n/a",
          "id": "buttonInfo"
        }
      ],
      "format": "n/a",
      "id": "button"
    },
    "applyForm": {
      "name": "路線選擇",
      "type": "object",
      "value": {
        "applyCommuteRoute ": {
          "name": "申請路線",
          "type": "object",
          "value": {
            "option": {
              "name": "欄位選單項目",
              "type": "array",
              "value": [
                {
                  "routeName": {
                    "name": "路線項目",
                    "type": "string",
                    "value": "路線1",
                    "format": "n/a",
                    "id": "routeName"
                  },
                  "routeKey": {
                    "name": "路線key",
                    "type": "string",
                    "value": "1",
                    "format": "n/a",
                    "id": "routeKey"
                  },
                  "commuteDetail": {
                    "name": "路線資訊",
                    "type": "array",
                    "value": [
                      {
                        "name": "子路線資訊",
                        "type": "object",
                        "value": {
                          "startLocation": {
                            "name": "起始地點",
                            "type": "string",
                            "value": "竹東 ",
                            "format": "n/a",
                            "id": "startLocation"
                          },
                          "endLocation": {
                            "name": "結束地點",
                            "type": "string",
                            "value": "竹北",
                            "format": "n/a",
                            "id": "endLocation"
                          },
                          "transportation": {
                            "name": "交通工具",
                            "type": "string",
                            "value": "計程車",
                            "format": "n/a",
                            "id": "transportation"
                          }
                        },
                        "format": "n/a",
                        "id": "subRoute"
                      },
                      {
                        "name": "子路線資訊",
                        "type": "object",
                        "value": {
                          "startLocation": {
                            "name": "起始地點",
                            "type": "string",
                            "value": "竹北 ",
                            "format": "n/a",
                            "id": "startLocation"
                          },
                          "endLocation": {
                            "name": "結束地點",
                            "type": "string",
                            "value": "台北",
                            "format": "n/a",
                            "id": "endLocation"
                          },
                          "transportation": {
                            "name": "交通工具",
                            "type": "string",
                            "value": "高鐵",
                            "format": "n/a",
                            "id": "transportation"
                          }
                        },
                        "format": "n/a",
                        "id": "subRoute"
                      },
                      {
                        "name": "子路線資訊",
                        "type": "object",
                        "value": {
                          "startLocation": {
                            "name": "起始地點",
                            "type": "string",
                            "value": "台北車站 ",
                            "format": "n/a",
                            "id": "startLocation"
                          },
                          "endLocation": {
                            "name": "結束地點",
                            "type": "string",
                            "value": "英特內軟體股份有限公司",
                            "format": "n/a",
                            "id": "endLocation"
                          },
                          "transportation": {
                            "name": "交通工具",
                            "type": "string",
                            "value": "捷運",
                            "format": "n/a",
                            "id": "transportation"
                          }
                        },
                        "format": "n/a",
                        "id": "subRoute"
                      }
                    ],
                    "format": "n/a",
                    "id": "commuteDetail"
                  }
                },
                {
                  "routeName": {
                    "name": "路線項目",
                    "type": "string",
                    "value": "其他",
                    "format": "n/a",
                    "id": "routeName"
                  },
                  "routeKey": {
                    "name": "路線key",
                    "type": "string",
                    "value": "999",
                    "format": "n/a",
                    "id": "routeKey"
                  },
                  "commuteDetail": {
                    "name": "路線資訊",
                    "type": "array",
                    "value": [
                      {
                        "name": "子路線資訊",
                        "type": "object",
                        "value": {
                          "startLocation": {
                            "name": "起始地點",
                            "type": "string",
                            "value": "竹東 ",
                            "format": "n/a",
                            "id": "startLocation"
                          },
                          "endLocation": {
                            "name": "結束地點",
                            "type": "string",
                            "value": "竹北",
                            "format": "n/a",
                            "id": "endLocation"
                          },
                          "transportation": {
                            "name": "交通工具",
                            "type": "string",
                            "value": "計程車",
                            "format": "n/a",
                            "id": "transportation"
                          }
                        },
                        "format": "n/a",
                        "id": "subRoute"
                      },
                      {
                        "name": "子路線資訊",
                        "type": "object",
                        "value": {
                          "startLocation": {
                            "name": "起始地點",
                            "type": "string",
                            "value": "竹北 ",
                            "format": "n/a",
                            "id": "startLocation"
                          },
                          "endLocation": {
                            "name": "結束地點",
                            "type": "string",
                            "value": "台北",
                            "format": "n/a",
                            "id": "endLocation"
                          },
                          "transportation": {
                            "name": "交通工具",
                            "type": "string",
                            "value": "高鐵",
                            "format": "n/a",
                            "id": "transportation"
                          }
                        },
                        "format": "n/a",
                        "id": "subRoute"
                      },
                      {
                        "name": "子路線資訊",
                        "type": "object",
                        "value": {
                          "startLocation": {
                            "name": "起始地點",
                            "type": "string",
                            "value": "台北車站 ",
                            "format": "n/a",
                            "id": "startLocation"
                          },
                          "endLocation": {
                            "name": "結束地點",
                            "type": "string",
                            "value": "英特內軟體股份有限公司",
                            "format": "n/a",
                            "id": "endLocation"
                          },
                          "transportation": {
                            "name": "交通工具",
                            "type": "string",
                            "value": "捷運",
                            "format": "n/a",
                            "id": "transportation"
                          }
                        },
                        "format": "n/a",
                        "id": "subRoute"
                      }
                    ],
                    "format": "n/a",
                    "id": "commuteDetail"
                  }
                }
              ],
              "format": "n/a",
              "id": "option"
            }
          },
          "format": "n/a",
          "id": "applyCommuteRoute"
        }
      },
      "format": "n/a",
      "id": "applyForm"
    },
    "properties": {
      "format": {
        "n/a": ""
      }
    }
  }
}
```

### HTTP Response when No Data 
無資料則屬於正常範圍，正常來說可以沒有資料,但在APP裡面需返回功能頁面
```json
{
   "status":"success",
   "message":[
      "查無資料"
   ],
   "data":{
      "beacon":{
         "name":"beacon",
         "type":"array",
         "value":[
            
         ],
         "format":"n/a",
         "id":"beacon"
      },
      "properties":{
         "format":{
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when UUID format error 
查詢資料中其一Beacon UUID格式錯誤 將返回錯誤訊息 beacon資訊為空
```json
{
   "status":"fail",
   "code":500,
   "message":[
      "Beacon設定檔有誤，UUID設定異常，請聯繫系統管理員檢查設定"
   ],
   "data":{
      "beacon":{
         "name":"beacon",
         "type":"array",
         "value":[
            
         ],
         "format":"n/a",
         "id":"beacon"
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
