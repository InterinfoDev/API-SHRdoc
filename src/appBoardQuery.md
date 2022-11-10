# appBoardQuery
取得公告詳細資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBoardQuery
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
| request | {seriesNo:D2} | Object | 查詢條件

### JSON representation

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "seriesNo":"D2"
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
| Case No | Key | Value | Type | Description | Required | Format |
|:----------|:----------|:-------------|:-----|:------------|:------------|:------------|
| 1 | seriesNo | 202112 | String | 公告序號 | Y | n/a |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "properties":{
         "format":{
            "HHmm":"時間時分",
            "YYYYmmdd":"西元年月日",
            "n/a":""
         }
      },
      "board":{
         "name":"公告詳細資料",
         "type":"object",
         "value":{
            "files":{
               "name":"參考檔案",
               "type":"array",
               "value":[
                  {
                     "fileType":{
                        "name":"檔案類型",
                        "type":"string",
                        "value":"",
                        "format":"n/a",
                        "id":"fileType"
                     },
                     "fileUrl":{
                        "name":"檔案路徑",
                        "type":"string",
                        "value":"",
                        "format":"n/a",
                        "id":"fileUrl"
                     },
                     "fileName":{
                        "name":"檔案名稱",
                        "type":"string",
                        "value":"",
                        "format":"n/a",
                        "id":"fileName"
                     }
                  }
               ],
               "format":"n/a",
               "id":"files"
            },
            "publisher":{
               "name":"公告人員工號",
               "type":"string",
               "value":"admin",
               "format":"n/a",
               "id":"publisher"
            },
            "category":{
               "name":"公告類別",
               "type":"string",
               "value":"行政",
               "format":"n/a",
               "id":"category"
            },
            "picture":{         --richard 修改格式
               "name":"公告圖片",
               "type":"string",
               "value": "http://59.124.100.151:8090/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f055d5e5d46535051635956535a4c637d0d110e11d794b4dabeb8daa991630e0909080c08070b0c080e0b0760485e4b5a4d6b4a4d4b535a11554f58",
               "format": "hyperlink",
               "id":"picture"
            },
            "publishTime":{
               "name":"公告時間",
               "type":"string",
               "value":"1404",
               "format":"HHmm",
               "id":"publishTime"
            },
            "publishDate":{
               "name":"公告日期",
               "type":"string",
               "value":"20211230",
               "format":"YYYYmmdd",
               "id":"publishDate"
            },
            "seriesNo":{
               "name":"公告序號",
               "type":"string",
               "value":"D2",
               "format":"n/a",
               "id":"seriesNo"
            },
            "article":{
               "name":"公告內文",
               "type":"string",
               "value":"xxxxxxxx",
               "format":"n/a",
               "id":"article"
            },
            "publisherName":{
               "name":"公告人員名稱",
               "type":"string",
               "value":"系O管",
               "format":"n/a",
               "id":"publisherName"
            },
            "subject":{
               "name":"公告主旨",
               "type":"string",
               "value":"xxxxx",
               "format":"n/a",
               "id":"subject"
            },
            "effectiveDate":{
               "name":"公告有效日期",
               "type":"string",
               "value":"20990630",
               "format":"YYYYmmdd",
               "id":"effectiveDate"
            }
         },
         "format":"n/a",
         "id":"board"
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於正常範圍，正常來說可以沒有資料
```json
{
   "status":"fail",
   "message":[
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
