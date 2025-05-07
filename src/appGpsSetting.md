# appGpsSetting
取得GPS打卡資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appGpsSetting
```

### HTTP Request Method
```
POST
```

### Request body
| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {} | Object | n/a |

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

### HTTP Response when Successful

```

### HTTP Response when Successful2
```json
{
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "properties": {
      "format": {
        "n/a": ""
      }
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
