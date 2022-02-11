# appUserVacationInfo
新增假別畫面以及假別欄位跟特殊日期的欄位檢核，查詢使用者假別資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appUserVacationInfo
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
| request | {hcode:, specialDate:} | Object | 查詢條件(依據畫面上使用者所選取的假別去取得假別代碼跟特殊日期)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "hcode":"", 
        "specialDate":""
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
| specialDate |  | String | 特殊日期 | N | AC(YYYYmm) |
| hcode |  | String | 假別代碼 | N | n/a |


### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "userInfo": {
            "name": "使用者資訊",
            "type": "object",
            "value": {
                "empFullName": {
                    "name": "員工中文姓名",
                    "type": "string",
                    "value": "系O管",
                    "format": "n/a",
                    "id": "empFullName"
                },
                "empid": {
                    "name": "員工編號",
                    "type": "string",
                    "value": "admin",
                    "format": "n/a",
                    "id": "empid"
                }
            },
            "format": "n/a",
            "id": "userInfo"
        },
        "properties": {
            "format": {
                "hour": "小時",
                "YYYYmmdd": "西元年月日",
                "day": "天",
                "n/a": ""
            }
        },
        "showSpecialDate": {
            "name": "是否顯示特殊日期",
            "type": "boolean",
            "value": false,
            "format": "n/a",
            "id": "showSpecialDate"
        },
        "usedVacationInfo": {
            "name": "假別使用資訊",
            "type": "array",
            "value": [
                {
                    "name": "特休資訊",
                    "type": "array",
                    "value": [
                        {
                            "name": "核休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "當年度特休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "approve"
                        },
                        {
                            "name": "已休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "已休(含在途)",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "used"
                        },
                        {
                            "name": "未休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "未休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "untaken"
                        },
                        {
                            "name": "備註",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "20221231",
                                    "format": "YYYYmmdd",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "當年度可保留期限",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "note"
                        }
                    ],
                    "format": "n/a",
                    "id": "annualLeave"
                },
                {
                    "name": "去年保留特休資訊",
                    "type": "array",
                    "value": [
                        {
                            "name": "核休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "56.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "當年度特休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "approve"
                        },
                        {
                            "name": "已休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "已休(含在途)",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "used"
                        },
                        {
                            "name": "未休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "56.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "未休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "untaken"
                        },
                        {
                            "name": "備註",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "20221231",
                                    "format": "YYYYmmdd",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "去年度可保留期限",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "note"
                        }
                    ],
                    "format": "n/a",
                    "id": "lastYearAnnualLeave"
                },
                {
                    "name": "彈休資訊",
                    "type": "array",
                    "value": [
                        {
                            "name": "核休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "當年度彈休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "approve"
                        },
                        {
                            "name": "已休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "已休(含在途)",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "used"
                        },
                        {
                            "name": "未休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "day",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "未休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "untaken"
                        }
                    ],
                    "format": "n/a",
                    "id": "floatingLeave"
                },
                {
                    "name": "加班補休資訊",
                    "type": "array",
                    "value": [
                        {
                            "name": "核休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "hour",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "當月加班補休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "approve"
                        },
                        {
                            "name": "已休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "hour",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "已休(含在途)",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "used"
                        },
                        {
                            "name": "未休",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "hour",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "累計未休",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "untaken"
                        },
                        {
                            "name": "當月預備轉結薪資時數",
                            "type": "object",
                            "value": {
                                "content": {
                                    "name": "內容",
                                    "type": "string",
                                    "value": "0.00",
                                    "format": "小時",
                                    "id": "content"
                                },
                                "title": {
                                    "name": "標題",
                                    "type": "string",
                                    "value": "當月預備轉結薪資時數",
                                    "format": "n/a",
                                    "id": "title"
                                }
                            },
                            "format": "n/a",
                            "id": "transToMoney"
                        }
                    ],
                    "format": "n/a",
                    "id": "floatingLeave"
                }
            ],
            "format": "n/a",
            "id": "usedVacationInfo"
        }
    }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，不會有查無資料情況
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
