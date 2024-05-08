# appOvertimeField
實際加班單申請畫面欄位

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appOvertimeField
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
| request | {empid:admin, overplanPno:xxx} | Object | 查詢條件(依據申請畫面取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "overplanPno":""
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
| overplanPno |  | String | 預定加班單號 | N | n/a |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "overtimeOverview": {
            "name": "加班總覽",
            "type": "object",
            "value": {
                "totalAmt": {
                    "name": "本次申請總時數",
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
                            "value": "1.500000",
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
                    "id": "totalAmt"
                },
                "appliedHour": {
                    "name": "當月已累積加班時數(不含本次)",
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
                            "value": "0.00",
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
                    "id": "appliedHour"
                },
                "threeMonthsApplyHours": {
                    "name": "當月已累積加班時數(不含本次)",
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
                            "value": "",
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": false,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "threeMonthsApplyHours"
                },
                "overDate": {
                    "name": "加班日期",
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
                            "value": "20240112",
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
                    "id": "overDate"
                }
            },
            "format": "n/a",
            "id": "overtimeOverview"
        },
        "punchCard": {
            "name": "刷卡資訊",
            "type": "object",
            "value": {
                "punchRecord": {
                    "name": "刷卡紀錄",
                    "type": "string",
                    "value": "進:1900 出:2230 ",
                    "format": "n/a",
                    "id": "punchRecord"
                },
                "punchDate": {
                    "name": "刷卡日期",
                    "type": "string",
                    "value": "20240112",
                    "format": "YYYYmmdd",
                    "id": "punchDate"
                },
                "punchIn": {
                    "name": "進卡時間",
                    "type": "string",
                    "value": "19:00",
                    "format": "n/a",
                    "id": "punchIn"
                },
                "punchOut": {
                    "name": "出卡時間",
                    "type": "string",
                    "value": "22:30",
                    "format": "n/a",
                    "id": "punchOut"
                }
            },
            "format": "n/a",
            "id": "punchCard"
        },
        "holidayRateDetail": {
            "name": "假日加班倍率資訊",
            "type": "array",
            "value": [
                {
                    "name": "假日第一段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.000000",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "holidayRate1"
                },
                {
                    "name": "假日第二段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.333400",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "holidayRate2"
                },
                {
                    "name": "假日第三段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.666700",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "holidayRate3"
                },
                {
                    "name": "假日第四段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.666700",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "holidayRate4"
                }
            ],
            "format": "n/a",
            "id": "holidayRateDetail"
        },
        "dailyRateDetail": {
            "name": "平日加班倍率資訊",
            "type": "array",
            "value": [
                {
                    "name": "平日第一段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.000000",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "dailyRate1"
                },
                {
                    "name": "平日第二段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "1.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.333400",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "dailyRate2"
                },
                {
                    "name": "平日第三段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.666700",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "dailyRate3"
                },
                {
                    "name": "平日第四段倍率時數",
                    "type": "object",
                    "value": {
                        "fieldValue": {
                            "name": "欄位預設值",
                            "type": "string",
                            "value": "0.000000",
                            "format": "hour",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "1.666700",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "dailyRate4"
                }
            ],
            "format": "n/a",
            "id": "dailyRateDetail"
        },
        "overtimeForm": {
            "name": "實際加班單填寫欄位資訊",
            "type": "object",
            "value": {
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
                            "value": "2000",
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
                "beforeWork": {
                    "name": "跨日往前加班",
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
                    "id": "beforeWork"
                },
                "earlyLeave": {
                    "name": "申請提早退勤(加班時數=實際出勤時數)",
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
                            "value": true,
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
                    "id": "earlyLeave"
                },
                "allowanceClass": {
                    "name": "津貼班別",
                    "type": "object",
                    "value": {
                        "option": {
                            "name": "選項",
                            "type": "array",
                            "value": [
                                {
                                    "optionId": {
                                        "name": "選項代號",
                                        "type": "string",
                                        "value": "D",
                                        "format": "n/a",
                                        "id": "optionId"
                                    },
                                    "optionValue": {
                                        "name": "選項名稱",
                                        "type": "string",
                                        "value": "總公司班",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                }
                            ],
                            "format": "n/a",
                            "id": "option"
                        },
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
                    "id": "allowanceClass"
                },
                "overtimeDepartment": {
                    "name": "加班部門",
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
                            "value": "283",
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldDisplay": {
                            "name": "欄位顯示資料",
                            "type": "string",
                            "value": "283 噠噠專屬部",
                            "format": "n/a",
                            "id": "fieldDisplay"
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
                    "id": "overtimeDepartment"
                },
                "reason": {
                    "name": "加班內容",
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
                            "value": "測試給付方式都可",
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
                    "id": "reason"
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
                            "value": "2130",
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
                "naturalDisaster": {
                    "name": "天災",
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
                    "id": "naturalDisaster"
                },
                "approvedProject": {
                    "name": "核准文號",
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
                            "value": false,
                            "format": "n/a",
                            "id": "fieldVisible"
                        }
                    },
                    "format": "n/a",
                    "id": "approvedProject"
                },
                "uploadFile": {
                    "name": "附件上傳",
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
                            "type": "array",
                            "value": [],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "uploadLimit": {
                            "name": "檔案上傳數量限制",
                            "type": "integer",
                            "value": 1,
                            "format": "count",
                            "id": "uploadLimit"
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
                    "id": "uploadFile"
                },
                "overtimeType": {
                    "name": "加班類別",
                    "type": "object",
                    "value": {
                        "option": {
                            "name": "選項",
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
                                        "value": "一般加班",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                },
                                {
                                    "optionId": {
                                        "name": "選項代號",
                                        "type": "string",
                                        "value": "B",
                                        "format": "n/a",
                                        "id": "optionId"
                                    },
                                    "optionValue": {
                                        "name": "選項名稱",
                                        "type": "string",
                                        "value": "特殊加班",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                },
                                {
                                    "optionId": {
                                        "name": "選項代號",
                                        "type": "string",
                                        "value": "C",
                                        "format": "n/a",
                                        "id": "optionId"
                                    },
                                    "optionValue": {
                                        "name": "選項名稱",
                                        "type": "string",
                                        "value": "專案加班",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                }
                            ],
                            "format": "n/a",
                            "id": "option"
                        },
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
                            "value": "A",
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
                    "id": "overtimeType"
                }
            },
            "format": "n/a",
            "id": "overtimeForm"
        },
        "payForm": {
            "name": "給付欄位資訊",
            "type": "object",
            "value": {
                "totalRestHour": {
                    "name": "總計補休時數",
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
                            "value": "0.500000",
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
                    "id": "totalRestHour"
                },
                "payType": {
                    "name": "給付方式",
                    "type": "object",
                    "value": {
                        "option": {
                            "name": "選項",
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
                                        "value": "補休",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                },
                                {
                                    "optionId": {
                                        "name": "選項代號",
                                        "type": "string",
                                        "value": "B",
                                        "format": "n/a",
                                        "id": "optionId"
                                    },
                                    "optionValue": {
                                        "name": "選項名稱",
                                        "type": "string",
                                        "value": "給薪",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                },
                                {
                                    "optionId": {
                                        "name": "選項代號",
                                        "type": "string",
                                        "value": "C",
                                        "format": "n/a",
                                        "id": "optionId"
                                    },
                                    "optionValue": {
                                        "name": "選項名稱",
                                        "type": "string",
                                        "value": "都有",
                                        "format": "n/a",
                                        "id": "optionValue"
                                    }
                                }
                            ],
                            "format": "n/a",
                            "id": "option"
                        },
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
                            "value": "C",
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
                    "id": "payType"
                },
                "totalPayHour": {
                    "name": "總計給薪時數",
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
                            "value": "1.000000",
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
                    "id": "totalPayHour"
                }
            },
            "format": "n/a",
            "id": "payForm"
        },
        "overtimeInfo": {
            "name": "實際加班單顯示欄位資訊",
            "type": "object",
            "value": {
                "empid": {
                    "name": "員工編號",
                    "type": "string",
                    "value": "T444",
                    "format": "n/a",
                    "id": "empid"
                },
                "overplanPno": {
                    "name": "預定加班單號",
                    "type": "string",
                    "value": "W002024011200001",
                    "format": "n/a",
                    "id": "overplanPno"
                },
                "attendClass": {
                    "name": "出勤班別",
                    "type": "string",
                    "value": "D 總公司班",
                    "format": "n/a",
                    "id": "attendClass"
                },
                "empFullName": {
                    "name": "員工中文姓名",
                    "type": "string",
                    "value": "光OO",
                    "format": "n/a",
                    "id": "empFullName"
                },
                "depFullName": {
                    "name": "部門名稱",
                    "type": "string",
                    "value": "噠噠專屬部",
                    "format": "n/a",
                    "id": "depFullName"
                },
                "companyId": {
                    "name": "公司代號",
                    "type": "string",
                    "value": "1",
                    "format": "n/a",
                    "id": "companyId"
                },
                "empFullEname": {
                    "name": "員工英文姓名",
                    "type": "string",
                    "value": "LigOO",
                    "format": "n/a",
                    "id": "empFullEname"
                },
                "depCode": {
                    "name": "部門代號",
                    "type": "string",
                    "value": "283",
                    "format": "n/a",
                    "id": "depCode"
                },
                "companyFullName": {
                    "name": "公司全名",
                    "type": "string",
                    "value": "三澧企業股份有限公司",
                    "format": "n/a",
                    "id": "companyFullName"
                }
            },
            "format": "n/a",
            "id": "overtimeInfo"
        },
        "properties": {
            "format": {
                "HHmm": "時間時分",
                "currency": "元",
                "hour": "小時",
                "YYYYmmdd": "西元年月日",
                "count": "數量",
                "n/a": ""
            }
        },
        "overtimeTip": {
            "name": "加班單備註",
            "type": "array",
            "value": [
                {
                    "name": "備註事項",
                    "type": "string",
                    "value": "平日加班",
                    "format": "n/a",
                    "id": "note"
                }
            ],
            "format": "n/a",
            "id": "overtimeTip"
        },
        "diningForm": {
            "name": "用餐欄位資訊",
            "type": "object",
            "value": {
                "newEatHour": {
                    "name": "新用餐時間",
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
                            "value": "",
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
                    "id": "newEatHour"
                },
                "specifyHour": {
                    "name": "指定用餐時間",
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
                    "id": "specifyHour"
                },
                "oldEatHour": {
                    "name": "原用餐時間",
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
                            "value": "0.00",
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
                    "id": "oldEatHour"
                },
                "misAmt": {
                    "name": "誤餐費",
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
                            "value": "0",
                            "format": "currency",
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
                    "id": "misAmt"
                },
                "isEat": {
                    "name": "是否用餐",
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
                            "value": true,
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
                    "id": "isEat"
                }
            },
            "format": "n/a",
            "id": "diningForm"
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
