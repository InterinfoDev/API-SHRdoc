# appAnnouncement
查詢通知訊息資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAnnouncement
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
| request | {announcementKey:0BB562CB-E166-4D69-9C50-C0EDF2511A38, announcementCount:10} | Object | 查詢條件

### JSON representation
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "announcementKey":"0BB562CB-E166-4D69-9C50-C0EDF2511A38",
        "announcementCount":10
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
 Key | Value | Type | Description | Required | Format |
|:----------|:-------------|:-----|:------------|:------------|:------------|
| announcementKey | 0BB562CB-E166-4D69-9C50-C0EDF2511A38 | String | 查詢最後一筆通知ID | N | n/a |  |
| announcementCount | 5 | Integer | 查詢資料筆數 | N | n/a | 預設筆數5 |
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
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        },
        "announcementList": {
            "name": "通知列表",
            "type": "array",
            "value": [
                {
                    "name": "通知資訊",
                    "type": "object",
                    "value": {
                        "sendTime": {
                            "name": "發送時間",
                            "type": "string",
                            "value": "0718",
                            "format": "HHmm",
                            "id": "sendTime"
                        },
                        "content": {
                            "name": "通知內容",
                            "type": "string",
                            "value": "第六筆 測試資料",
                            "format": "n/a",
                            "id": "content"
                        },
                        "announcementKey": {
                            "name": "通知編號",
                            "type": "string",
                            "value": "0BB562CB-E166-4D69-9C50-C0EDF2511A38",
                            "format": "n/a",
                            "id": "announcementKey"
                        },
                        "sendDate": {
                            "name": "發送日期",
                            "type": "string",
                            "value": "20220225",
                            "format": "YYYYmmdd",
                            "id": "sendDate"
                        },
                        "sendEmpFullName": {
                            "name": "發送者中文姓名",
                            "type": "string",
                            "value": "系O管",
                            "format": "n/a",
                            "id": "sendEmpFullName"
                        },
                        "sendEmpid": {
                            "name": "發送者編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "sendEmpid"
                        }
                    },
                    "format": "n/a",
                    "id": "announcement"
                },
                {
                    "name": "通知資訊",
                    "type": "object",
                    "value": {
                        "sendTime": {
                            "name": "發送時間",
                            "type": "string",
                            "value": "0718",
                            "format": "HHmm",
                            "id": "sendTime"
                        },
                        "content": {
                            "name": "通知內容",
                            "type": "string",
                            "value": "第七筆 測試資料",
                            "format": "n/a",
                            "id": "content"
                        },
                        "announcementKey": {
                            "name": "通知編號",
                            "type": "string",
                            "value": "6ECC6826-3A2C-45CF-93C9-21A14D515C09",
                            "format": "n/a",
                            "id": "announcementKey"
                        },
                        "sendDate": {
                            "name": "發送日期",
                            "type": "string",
                            "value": "20220226",
                            "format": "YYYYmmdd",
                            "id": "sendDate"
                        },
                        "sendEmpFullName": {
                            "name": "發送者中文姓名",
                            "type": "string",
                            "value": "系O管",
                            "format": "n/a",
                            "id": "sendEmpFullName"
                        },
                        "sendEmpid": {
                            "name": "發送者編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "sendEmpid"
                        }
                    },
                    "format": "n/a",
                    "id": "announcement"
                },
                {
                    "name": "通知資訊",
                    "type": "object",
                    "value": {
                        "sendTime": {
                            "name": "發送時間",
                            "type": "string",
                            "value": "0718",
                            "format": "HHmm",
                            "id": "sendTime"
                        },
                        "content": {
                            "name": "通知內容",
                            "type": "string",
                            "value": "第八筆 測試資料",
                            "format": "n/a",
                            "id": "content"
                        },
                        "announcementKey": {
                            "name": "通知編號",
                            "type": "string",
                            "value": "712B2A1B-439B-4AC8-A927-1C072A136DC7",
                            "format": "n/a",
                            "id": "announcementKey"
                        },
                        "sendDate": {
                            "name": "發送日期",
                            "type": "string",
                            "value": "20220226",
                            "format": "YYYYmmdd",
                            "id": "sendDate"
                        },
                        "sendEmpFullName": {
                            "name": "發送者中文姓名",
                            "type": "string",
                            "value": "系O管",
                            "format": "n/a",
                            "id": "sendEmpFullName"
                        },
                        "sendEmpid": {
                            "name": "發送者編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "sendEmpid"
                        }
                    },
                    "format": "n/a",
                    "id": "announcement"
                },
                {
                    "name": "通知資訊",
                    "type": "object",
                    "value": {
                        "sendTime": {
                            "name": "發送時間",
                            "type": "string",
                            "value": "0718",
                            "format": "HHmm",
                            "id": "sendTime"
                        },
                        "content": {
                            "name": "通知內容",
                            "type": "string",
                            "value": "第九筆 測試資料",
                            "format": "n/a",
                            "id": "content"
                        },
                        "announcementKey": {
                            "name": "通知編號",
                            "type": "string",
                            "value": "BA1EF1EC-0470-4A33-B89B-6079B69CFD29",
                            "format": "n/a",
                            "id": "announcementKey"
                        },
                        "sendDate": {
                            "name": "發送日期",
                            "type": "string",
                            "value": "20220226",
                            "format": "YYYYmmdd",
                            "id": "sendDate"
                        },
                        "sendEmpFullName": {
                            "name": "發送者中文姓名",
                            "type": "string",
                            "value": "系O管",
                            "format": "n/a",
                            "id": "sendEmpFullName"
                        },
                        "sendEmpid": {
                            "name": "發送者編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "sendEmpid"
                        }
                    },
                    "format": "n/a",
                    "id": "announcement"
                },
                {
                    "name": "通知資訊",
                    "type": "object",
                    "value": {
                        "sendTime": {
                            "name": "發送時間",
                            "type": "string",
                            "value": "0719",
                            "format": "HHmm",
                            "id": "sendTime"
                        },
                        "content": {
                            "name": "通知內容",
                            "type": "string",
                            "value": "第十筆 測試資料",
                            "format": "n/a",
                            "id": "content"
                        },
                        "announcementKey": {
                            "name": "通知編號",
                            "type": "string",
                            "value": "93E11C77-11E2-4A3D-BA42-3E19AE04164D",
                            "format": "n/a",
                            "id": "announcementKey"
                        },
                        "sendDate": {
                            "name": "發送日期",
                            "type": "string",
                            "value": "20220226",
                            "format": "YYYYmmdd",
                            "id": "sendDate"
                        },
                        "sendEmpFullName": {
                            "name": "發送者中文姓名",
                            "type": "string",
                            "value": "系O管",
                            "format": "n/a",
                            "id": "sendEmpFullName"
                        },
                        "sendEmpid": {
                            "name": "發送者編號",
                            "type": "string",
                            "value": "admin",
                            "format": "n/a",
                            "id": "sendEmpid"
                        }
                    },
                    "format": "n/a",
                    "id": "announcement"
                }
            ],
            "format": "n/a",
            "id": "announcementList"
        }
    }
}
```

### HTTP Response when No Data
無資料則屬於正常情況
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
                "YYYYmmdd": "西元年月日",
                "n/a": ""
            }
        },
        "announcementList": {
            "name": "通知列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "announcementList"
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
