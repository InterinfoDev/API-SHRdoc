# appVacationDetail
查詢該假單詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationDetail
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
| request | {pno:W00202201250001, empid:admin} | Object | 查詢條件(依據使用者所選擇要查看的假單單號及畫面上的員工編號)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "pno":"W00202201250001", 
        "empid":"admin"
    }
}
```

### Properties
| Property | Type | Description | 
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |
| request | Object | 要求本文 |

### fieldType
| Type | Description | key |
|:---------|:------------|:------------|
| text | 文字顯示類型  | fieldValue |
| file | 附件下載顯示類型 | files |
| switch | 開關類型 | switch |


### Request Properties
| Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| pno | W00202201250001 | String | 單據編號 | Y | n/a |
| empid | admin | String | 員工編號 | Y | n/a |


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
                "day": "天",
                "n/a": ""
            }
        },
        "flowHistory": {
            "name": "流程紀錄",
            "type": "object",
            "value": {
                "historyKey": {
                    "name": "流程鍵值",
                    "type": "string",
                    "value": "4155331322073258637810082871479386793510277398195316129455310019418389165116920755637226659208981976243501804777343271423225872349584960",
                    "format": "n/a",
                    "id": "historyKey"
                }
            },
            "format": "n/a",
            "id": "flowHistory"
        },
        "vacationDetail": {
            "name": "請假單詳細資訊",
            "type": "object",
            "value": [
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "pno",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "W00202405070002"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "單號",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "companyFullName",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "三澧企業股份有限公司"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "公司別",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "empFullName",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "AOO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "員工姓名",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "empFullEname",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "TESOO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldVisible": {
                            "name": "欄位顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "fieldVisible"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "員工英文姓名",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "depFullName",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "台北總公司"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "部門別",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "vacationName",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "無薪病假(TEST)-住院(測試兩年病假)"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "假別",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "vacationStartTime",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "2024/06/01 18:00"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "起始時間",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "vacationEndTime",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "2024/06/01 19:00"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "結束時間",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "amt",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "1.00 天"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "請假時數",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "reason",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "test"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "請假原因",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "delayReason",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                ""
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "逾時原因",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "isHoliday",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "switch": {
                            "name": "開關",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "switch"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "是否包含假日",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "planeTicket",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "0"
                            ],
                            "format": "ticket",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "機票",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "jobAgent",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "8746546 李OO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "職務代理人",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "flowAgent",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "870461689 李OO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "簽核代理人",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "flowAgent1",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "875465409 李OO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "簽核代理人1",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "flowAgent2",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "8754649 李OO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "簽核代理人2",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "text",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "flowAgent3",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "fieldValue": {
                            "name": "欄位資料",
                            "type": "array",
                            "value": [
                                "8703009 李OO"
                            ],
                            "format": "n/a",
                            "id": "fieldValue"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "簽核代理人3",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                },
                {
                    "name": "欄位資訊",
                    "type": "object",
                    "value": {
                        "fieldType": {
                            "name": "欄位類型",
                            "type": "string",
                            "value": "file",
                            "format": "n/a",
                            "id": "fieldType"
                        },
                        "fieldId": {
                            "name": "欄位代號",
                            "type": "string",
                            "value": "uploadFiles",
                            "format": "n/a",
                            "id": "fieldId"
                        },
                        "files": {
                            "name": "附件資訊",
                            "type": "array",
                            "value": [],
                            "format": "n/a",
                            "id": "files"
                        },
                        "fieldName": {
                            "name": "欄位名稱",
                            "type": "string",
                            "value": "附件",
                            "format": "n/a",
                            "id": "fieldName"
                        }
                    },
                    "format": "n/a",
                    "id": "field"
                }
            ],
            "format": "n/a",
            "id": "vacationDetail"
        }
    }
}
```

### HTTP Response when No Data 
無資料則屬於 Code 500 錯誤，因為前面查詢都有資料了
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
