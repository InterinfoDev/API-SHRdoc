# appVacationField
請假單申請畫面欄位

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appVacationField
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
| request | {specialDate:XXX, employeeId:admin, vacationCode:XXX, startDate:20230529} | Object | 查詢條件(依據申請畫面取得)

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "specialDate":"20230602", 
        "employeeId":"9306020",
        "vacationCode":"04a",
        "startDate":""
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
| specialDate | 20220425 | String | 特殊日期 | N | AC(YYYYmmdd) |
| employeeId | admin | String | 員工編號 | Y | n/a |
| vacationCode | 06.061 | String | 假別代碼 | Y | n/a |
| startDate | 20220425 | String | 起始日期 | N | AC(YYYYmmdd) |

### HTTP Response when Successful
```json
{
  "status": "success",
  "message": [
    "回傳成功"
  ],
  "data": {
    "vacationForm": {
      "name": "請假單填寫欄位資訊",
      "type": "object",
      "value": {
        "jobAgent": {
          "name": "職務代理人",
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
                    "value": "0014",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "儲OO",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "0007",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "曹OO",
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
              "value": "0310",
              "format": "n/a",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "jobAgent"
        },
        "vacationType": {
          "name": "請假類別",
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
                    "value": "3",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "其他",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "1",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "大陸（不含港澳）",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "2",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "其他國家（含港澳）",
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
              "value": "true",
              "format": "n/a",
              "id": "fieldEditable"
            },
            "fieldValue": {
              "name": "欄位預設值",
              "type": "string",
              "value": "3",
              "format": "n/a",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": "true",
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "vacationType"
        },
        "startDate": {
          "name": "起始日期",
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
              "value": "20240813",
              "format": "YYYYmmdd",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "startDate"
        },
        "outSideId": {
          "name": "相關單號",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "outSideId"
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
              "value": 5,
              "format": "count",
              "id": "uploadLimit"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "uploadFile"
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
              "value": "1830",
              "format": "HHmm",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "endTime"
        },
        "amt": {
          "name": "本次請假時間合計",
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
              "value": "9.00",
              "format": "hour",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "amt"
        },
        "place": {
          "name": "地點",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "place"
        },
        "isHoliday": {
          "name": "是否包含假日",
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
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "isHoliday"
        },
        "planeTicket": {
          "name": "機票",
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
              "format": "ticket",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "planeTicket"
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
              "value": "0930",
              "format": "HHmm",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "startTime"
        },
        "flowAgent3": {
          "name": "代理人三",
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
                    "value": "0014",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "儲OO",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "0007",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "曹OO",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "flowAgent3"
        },
        "flowAgent2": {
          "name": "代理人二",
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
                    "value": "0014",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "儲OO",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "0007",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "曹OO",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "flowAgent2"
        },
        "flowAgent1": {
          "name": "代理人一",
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
                    "value": "0014",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "儲OO",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "0007",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "曹OO",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "flowAgent1"
        },
        "familyName": {
          "name": "親屬姓名",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "familyName"
        },
        "flowAgent": {
          "name": "簽核代理人",
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
                    "value": "0014",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "儲OO",
                    "format": "n/a",
                    "id": "optionValue"
                  }
                },
                {
                  "optionId": {
                    "name": "選項代號",
                    "type": "string",
                    "value": "0007",
                    "format": "n/a",
                    "id": "optionId"
                  },
                  "optionValue": {
                    "name": "選項名稱",
                    "type": "string",
                    "value": "曹OO",
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
              "value": "",
              "format": "n/a",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "flowAgent"
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
              "value": "20240813",
              "format": "YYYYmmdd",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "endDate"
        },
        "reason": {
          "name": "請假原因",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": true,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "reason"
        },
        "delayReason": {
          "name": "逾時請假原因",
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
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "delayReason"
        }
      },
      "format": "n/a",
      "id": "vacationForm"
    },
    "vacationSpecForm": {
      "name": "請假單其他資訊",
      "type": "object",
      "value": {
        "specialDate": {
          "name": "特殊日期",
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
              "value": "20230602",
              "format": "YYYYmmdd",
              "id": "fieldValue"
            },
            "fieldVisible": {
              "name": "欄位顯示",
              "type": "boolean",
              "value": false,
              "format": "n/a",
              "id": "fieldVisible"
            }
          },
          "format": "n/a",
          "id": "specialDate"
        }
      },
      "format": "n/a",
      "id": "vacationSpecForm"
    },
    "properties": {
      "format": {
        "HHmm": "時間時分",
        "hour": "小時",
        "YYYYmmdd": "西元年月日",
        "count": "數量",
        "n/a": "",
        "ticket": "張"
      }
    },
    "vacationInfo": {
      "name": "請假單顯示欄位資訊",
      "type": "object",
      "value": {
        "vacationName": {
          "name": "假別名稱",
          "type": "string",
          "value": "事假中和",
          "format": "n/a",
          "id": "vacationName"
        },
        "depCode": {
          "name": "部門代號",
          "type": "string",
          "value": "99999",
          "format": "n/a",
          "id": "depCode"
        },
        "vacationCode": {
          "name": "假別代碼",
          "type": "string",
          "value": "01",
          "format": "n/a",
          "id": "vacationCode"
        },
        "companyFullName": {
          "name": "公司全名",
          "type": "string",
          "value": "72英特內全名(中和)軟體股份有限公司",
          "format": "n/a",
          "id": "companyFullName"
        },
        "empFullName": {
          "name": "員工中文姓名",
          "type": "string",
          "value": "李OO",
          "format": "n/a",
          "id": "empFullName"
        },
        "employeeId": {
          "name": "員工編號",
          "type": "string",
          "value": "admin",
          "format": "n/a",
          "id": "employeeId"
        },
        "depFullName": {
          "name": "部門名稱",
          "type": "string",
          "value": "英特內股份有限公司",
          "format": "n/a",
          "id": "depFullName"
        },
        "empFullEname": {
          "name": "員工英文姓名",
          "type": "string",
          "value": "AdmOO",
          "format": "n/a",
          "id": "empFullEname"
        }
      },
      "format": "n/a",
      "id": "vacationInfo"
    },
    "vacationTip": {
      "name": "請假單備註",
      "type": "array",
      "value": [
        {
          "name": "備註事項",
          "type": "string",
          "value": "特休請完，才能請事假.",
          "format": "n/a",
          "id": "note"
        }
      ],
      "format": "n/a",
      "id": "vacationTip"
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
