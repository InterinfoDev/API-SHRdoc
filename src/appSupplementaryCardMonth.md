# appSupplementaryCardMonth
取得員工補卡資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appSupplementaryCardMonth
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
| request | {cardYM:202111, empid:['admin'] , companyId:'97090920' , depNumber:[]} | Object | 查詢條件

### JSON representation
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "cardYM":"2021906",
        "companyId":"97090920"
        "empid":["admin"],
        "depNumber":[]
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
| empid | [admin] | Array(String) | 員工編號 | N | n/a | 查詢員工編號 |
| depNumber | [5] | Array(Integer) | 部門代號 | N | n/a |
| companyId | 97090920 | String | 公司別 | N | n/a |
| cardYM | 202106 | String | 查詢年月 | Y | AC(YYYYmm) |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "main": {
            "name": "請假資訊",
            "type": "object",
            "value": {
                "cardYM": {
                    "name": "補卡年月",
                    "type": "string",
                    "value": "202106",
                    "format": "YYYYmm",
                    "id": "cardYM"
                }
            },
            "format": "n/a",
            "id": "main"
        },
        "cardList": {
            "name": "員工補卡列表",
            "type": "array",
            "value": [
                {
                    "name": "員工補卡資訊",
                    "type": "object",
                    "value": {
                        "position": {
                            "name": "職稱",
                            "type": "string",
                            "value": "短期契約",
                            "format": "n/a",
                            "id": "position"
                        },
                        "unapproved": {
                            "name": "簽核中",
                            "type": "integer",
                            "value": 2,
                            "format": "count",
                            "id": "unapproved"
                        },
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
                        },
                        "photo": {
                            "name": "員工照片",
                            "type": "string",
                            "value": "http://59.124.100.151:8090/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f1a574d52104f57504b50100e0909070f0b0b0607070b0b07600e0b0f070f060e0e0d114f5158",
                            "format": "hyperlink",
                            "id": "photo"
                        },
                        "approved": {
                            "name": "已生效",
                            "type": "integer",
                            "value": 0,
                            "format": "count",
                            "id": "approved"
                        },
                        "depFullName": {
                            "name": "部門名稱",
                            "type": "string",
                            "value": "L1線A班",
                            "format": "n/a",
                            "id": "depFullName"
                        }
                    },
                    "format": "n/a",
                    "id": "card"
                }
            ],
            "format": "count",
            "id": "cardList"
        },
        "properties": {
            "format": {
                "count": "數量",
                "n/a": "",
                "YYYYmm": "西元年月",
                "hyperlink":"超連結"
            }
        }
    }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "main":{
         "name":"請假資訊",
         "type":"object",
         "value":{
            "cardYM":{
               "name":"補卡年月",
               "type":"string",
               "value":"202106",
               "format":"YYYYmm",
               "id":"cardYM"
            }
         },
         "format":"n/a",
         "id":"main"
      },
      "cardList":{
         "name":"員工補卡列表",
         "type":"array",
         "value":[
            
         ],
         "format":"count",
         "id":"cardList"
      },
      "properties":{
         "format":{
            "count":"數量",
            "n/a":"",
            "YYYYmm":"西元年月"
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
