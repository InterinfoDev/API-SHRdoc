# appTravelChangeField
出差變更單申請畫面欄位

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelChangeField
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
| request | {pno:XXX} | Object | 查詢條件(依據申請畫面取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "pno":"xxx"
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
| pno | xxx | String | 出差單編號 | Y | n/a |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "hour": "小時",
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        },
        "travelChangeForm": {
            "name": "出差基本欄位資訊",
            "type": "object",
            "value": {
                "amt": {
                    "name": "出差總計",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": false,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "8.00",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "amt"
                },
                "startTime": {
                    "name": "起始時間",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0900",
                            "format": "HHmm",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "startTime"
                },
                "startDate": {
                    "name": "行程規劃",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "20231117",
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "schedule"
                },
                "travelPlace": {
                    "name": "出差地點",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "Hjj",
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "travelPlace"
                },
                "endDate": {
                    "name": "結束日期",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "20231117",
                            "format": "YYYYmmdd",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "endDate"
                },
                "endTime": {
                    "name": "結束時間",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "1800",
                            "format": "HHmm",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "endTime"
                },
                "note": {
                    "name": "變更事由",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "",
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "note"
                },
                "isHoliday": {
                    "name": "是否包含假日",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "boolean",
                            "value": false,
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "isHoliday"
                },
                "isBusinessTrip": {
                    "name": "具公差性質",
                    "type": "object",
                    "value": {
                        "fieldEditable": {
                            "name": "開放編輯",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldEditable"
                        },
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "boolean",
                            "value": false,
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "isBusinessTrip"
                }
            },
            "format": "n/a",
            "id": "travelChangeForm"
        },
        "travelChangeInfo": {
            "name": "出差異動單顯示欄位資訊",
            "type": "object",
            "value": {
                "pno": {
                    "name": "變更單號",
                    "type": "string",
                    "value": "K00202311030001",
                    "format": "n/a",
                    "id": "position"
                },
                "empid": {
                    "name": "員工編號",
                    "type": "string",
                    "value": "T888",
                    "format": "n/a",
                    "id": "empid"
                },
                "position": {
                    "name": "職稱",
                    "type": "string",
                    "value": "噠噠測試組主管",
                    "format": "n/a",
                    "id": "position"
                },
                "version": {
                    "name": "變更版次",
                    "type": "string",
                    "value": "1",
                    "format": "n/a",
                    "id": "version"
                },
                "empFullName": {
                    "name": "員工中文姓名",
                    "type": "string",
                    "value": "夜OO",
                    "format": "n/a",
                    "id": "empFullName"
                },
                "oldPno": {
                    "name": "出差單號",
                    "type": "string",
                    "value": "K00202311030001",
                    "format": "n/a",
                    "id": "position"
                },
                "depFullName": {
                    "name": "部門名稱",
                    "type": "string",
                    "value": "噠噠測試組",
                    "format": "n/a",
                    "id": "depFullName"
                },
                "empFullEname": {
                    "name": "員工英文姓名",
                    "type": "string",
                    "value": "nigOO",
                    "format": "n/a",
                    "id": "empFullEname"
                },
                "depCode": {
                    "name": "部門代號",
                    "type": "string",
                    "value": "284",
                    "format": "n/a",
                    "id": "depCode"
                },
                "companyFullName": {
                    "name": "公司全名",
                    "type": "string",
                    "value": "xx企業股份有限公司",
                    "format": "n/a",
                    "id": "companyFullName"
                },
                "applyDate": {
                    "name": "變更日期",
                    "type": "string",
                    "value": "20240508",
                    "format": "YYYYmmdd",
                    "id": "applyDate"
                }
            },
            "format": "n/a",
            "id": "travelChangeInfo"
        },
        "travelForm": {
            "name": "出差異動單顯示欄位資訊",
            "type": "object",
            "value": {
                "startDate": {
                    "name": "起始日期",
                    "type": "string",
                    "value": "20231117",
                    "format": "YYYYmmdd",
                    "id": "startDate"
                },
                "endTime": {
                    "name": "結束時間",
                    "type": "string",
                    "value": "1800",
                    "format": "HHmm",
                    "id": "endTime"
                },
                "travelPlace": {
                    "name": "出差地點",
                    "type": "string",
                    "value": "Hjj",
                    "format": "n/a",
                    "id": "travelPlace"
                },
                "startTime": {
                    "name": "起始時間",
                    "type": "string",
                    "value": "0900",
                    "format": "HHmm",
                    "id": "startTime"
                },
                "endDate": {
                    "name": "結束日期",
                    "type": "string",
                    "value": "20231117",
                    "format": "YYYYmmdd",
                    "id": "endDate"
                },
                "amt": {
                    "name": "出差總計",
                    "type": "decimal",
                    "value": 8.0,
                    "format": "hour",
                    "id": "amt"
                }
            },
            "format": "n/a",
            "id": "travelForm"
        }
    }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有資料
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
