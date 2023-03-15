# appWorkPlace
取得使用者上班地點資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appWorkPlace
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


### JSON representation
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### HTTP Response when Successful
```json
{
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "workPlaceOptionList": {
      "name": "打卡項目清單",
      "type": "array",
      "value": [
        {
          "name": "打卡項目資訊",
          "type": "array",
          "value": [
            {
              "workCardCode": {
                "name": "打卡項目代碼",
                "type": "string",
                "value": "E1",
                "format": "n/a",
                "id": "workcardCode"
              },
              "workPlaceList": {
                "name": "工作地點資訊",
                "type": "object",
                "value": {
                  "location": {
                    "name": "工作位置",
                    "type": "string",
                    "value": [
                      {
                        "longitude": {
                          "name": "經度",
                          "type": "decimal",
                          "value": 121.4857181,
                          "format": "n/a",
                          "id": "longitude"
                        },
                        "latitude": {
                          "name": "緯度",
                          "type": "decimal",
                          "value": 24.9983947,
                          "format": "n/a",
                          "id": "latitude"
                        }
                      },
                      {
                        "longitude": {
                          "name": "經度",
                          "type": "decimal",
                          "value": 121.4857181,
                          "format": "n/a",
                          "id": "longitude"
                        },
                        "latitude": {
                          "name": "緯度",
                          "type": "decimal",
                          "value": 24.9983947,
                          "format": "n/a",
                          "id": "latitude"
                        }
                      }
                    ],
                    "format": "n/a",
                    "id": "location"
                  }
                },
                "format": "n/a",
                "id": "workPlaceList"
              },
              "workCardName": {
                "name": "打卡項目名稱",
                "type": "string",
                "value": "北車GPS",
                "format": "n/a",
                "id": "workcardName"
              }
            }
          ],
          "format": "n/a",
          "id": "workPlaceDetail"
        },
        {
          "name": "打卡項目資訊",
          "type": "array",
          "value": [
            {
              "workCardCode": {
                "name": "打卡項目代碼",
                "type": "string",
                "value": "D1",
                "format": "n/a",
                "id": "workcardCode"
              },
              "workPlaceList": {
                "name": "工作地點資訊",
                "type": "object",
                "value": {
                  "location": {
                    "name": "工作位置",
                    "type": "string",
                    "value": [
                      {
                        "longitude": {
                          "name": "經度",
                          "type": "decimal",
                          "value": 121.4857181,
                          "format": "n/a",
                          "id": "longitude"
                        },
                        "latitude": {
                          "name": "緯度",
                          "type": "decimal",
                          "value": 24.9983947,
                          "format": "n/a",
                          "id": "latitude"
                        }
                      },
                      {
                        "longitude": {
                          "name": "經度",
                          "type": "decimal",
                          "value": 121.4857181,
                          "format": "n/a",
                          "id": "longitude"
                        },
                        "latitude": {
                          "name": "緯度",
                          "type": "decimal",
                          "value": 24.9983947,
                          "format": "n/a",
                          "id": "latitude"
                        }
                      }
                    ],
                    "format": "n/a",
                    "id": "location"
                  }
                },
                "format": "n/a",
                "id": "workPlaceList"
              },
              "workCardName": {
                "name": "打卡項目名稱",
                "type": "string",
                "value": "英特內GPS-12F",
                "format": "n/a",
                "id": "workcardName"
              }
            }
          ],
          "format": "n/a",
          "id": "workPlaceDetail"
        }
      ],
      "format": "n/a",
      "id": "workCardItem"
    },
    "properties": {
      "format": {
        "n/a": "",
        "meter": "公尺"
      }
    },
    "workPlaceList": {
      "name": "工作地點清單",
      "type": "array",
      "value": [
        {
          "name": "工作地點資訊",
          "type": "object",
          "value": {
            "radius": {
              "name": "打卡半徑",
              "type": "decimal",
              "value": 0.1,
              "format": "meter",
              "id": "radius"
            },
            "location": {
              "name": "工作位置",
              "type": "object",
              "value": {
                "longitude": {
                  "name": "經度",
                  "type": "decimal",
                  "value": 121.4857181,
                  "format": "n/a",
                  "id": "longitude"
                },
                "latitude": {
                  "name": "緯度",
                  "type": "decimal",
                  "value": 24.9983947,
                  "format": "n/a",
                  "id": "latitude"
                }
              },
              "format": "n/a",
              "id": "location"
            },
            "placeName": {
              "name": "工作地點中文名稱",
              "type": "string",
              "value": "台北_南京東路辦公室",
              "format": "n/a",
              "id": "placeName"
            },
            "placeEname": {
              "name": "工作地點英文名稱",
              "type": "string",
              "value": "",
              "format": "n/a",
              "id": "placeEname"
            },
            "placeCode": {
              "name": "工作地點代號",
              "type": "string",
              "value": "B",
              "format": "n/a",
              "id": "placeCode"
            }
          },
          "format": "n/a",
          "id": "workPlace"
        }
      ],
      "format": "n/a",
      "id": "workPlaceList"
    }
  }
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
