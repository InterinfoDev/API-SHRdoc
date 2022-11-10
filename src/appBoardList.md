# appBoardList
取得公告清單資訊

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appBoardList
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
| request | {boardYM:202111} | Object | 查詢條件

### JSON representation

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820", 
    "request":{
        "boardYM":"202112"
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
| 1 | boardYM | 202112 | String | 年月 | Y | AC(YYYYmm) |

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
            "hyperlink":"超連結"
            "n/a":""
         }
      },
      "board":{
         "name":"公告資訊",
         "type":"object",
         "value":[
            {
               "name":"公告詳細資料",
               "type":"object",
               "value":{
                  "publishDate":{
                     "name":"公告日期",
                     "type":"string",
                     "value":"20150621",
                     "format":"YYYYmmdd",
                     "id":"publishDate"
                  },
                  "subject":{
                     "name":"公告主旨",
                     "type":"string",
                     "value":"xxxxx",
                     "format":"n/a",
                     "id":"subject"
                  },
                  "publisherName":{
                     "name":"公告人員名稱",
                     "type":"string",
                     "value":"xxx",
                     "format":"n/a",
                     "id":"publisherName"
                  },
                  "publisher":{
                     "name":"公告人員工號",
                     "type":"string",
                     "value":"admin",
                     "format":"n/a",
                     "id":"publisher"
                  },
                  "publishTime":{
                     "name":"公告時間",
                     "type":"string",
                     "value":"215501",
                     "format":"HHmm",
                     "id":"publishTime"
                  },
                  "picture":{         --richard 修改格式
                     "name":"公告圖片",
                     "type":"string",
                     "value": "http://59.124.100.151:8090/servlet/jform?em_step=2&file=hrm8w.pkg&enc=93d23f3a4b3f055d5e5d46535051635956535a4c637d0d110e11d794b4dabeb8daa991630e0909080c08070b0c080e0b0760485e4b5a4d6b4a4d4b535a11554f58",
                     "format": "hyperlink",
                     "id":"picture"
                  },
                  "seriesNo":{
                     "name":"公告序號",
                     "type":"string",
                     "value":"D2",
                     "format":"n/a",
                     "id":"seriesNo"
                  }
               },
               "format":"n/a",
               "id":"boardDetail"
            }
         ],
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
         "name":"公告資訊",
         "type":"object",
         "value":[
            
         ],
         "format":"n/a",
         "id":"board"
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
