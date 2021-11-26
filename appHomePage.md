# appHomePage

取得APP個人首頁資訊

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appHomePage
```

### HTTP Request Mehod
```
POST
```


### Request body

| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| uid | 98599308101484732326 | String | 需透過appLogin取得 |
| right | 51341911904173543336756162544864820... | String | 需透過appLogin取得 |


### JSON representation

Here is a JSON representation of request.

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820...
}
```


### Properties

| Property | Type | Description |
|:---------|:-----|:------------|
| **uid**   | String | 加密後帳號 |
| **right** | String | 加密後系統相關資料 |


### HTTP Response when Successful
```json
{
   "data":{
      "personal":{
         "id":"personalInfo",
         "name":"個人資訊",
         "value":{
            "empName":{
               "id":"empName",
               "name":"員工中文姓名",
               "value":"林奇杰",
               "type":"string",
               "format":"n/a"
            },
            "empEname":{
               "id":"empEname",
               "name":"員工英文姓名",
               "value":"Lucas",
               "type":"string",
               "format":"n/a"
            },
            "depCode":{
               "id":"deoCode",
               "name":"部門代號",
               "value":"D2000",
               "type":"string",
               "format":"n/a"
            },
            "depName":{
               "id":"depName",
               "name":"部門名稱",
               "value":"CTO",
               "type":"string",
               "format":"n/a"
            },
            "empid":{
               "id":"empid",
               "name":"員工編號",
               "value":"L100387",
               "type":"string",
               "format":"n/a"
            },
            "position":{
               "id":"position",
               "name":"職稱",
               "value":"CTO",
               "type":"string",
               "format":"n/a"
            },
            "photo":{
               "id":"photo",
               "name":"員工照片",
               "value":"",
               "type":"string",
               "format":"base64"
            }
         },
         "type":"object",
         "format":"n/a"
      },
      "attend":{
         "id":"attendInfo",
         "name":"考勤資訊",
         "value":[
            {
               "id":"20211001",
               "name":"20211001考勤資訊",
               "value":{
                  "workDate":{
                     "id":"workDate",
                     "name":"出勤日期",
                     "value":"20211001",
                     "type":"string",
                     "format":"n/a"
                  },
                  "workClass":{
                     "id":"workClass",
                     "name":"班別代號",
                     "value":"D",
                     "type":"string",
                     "format":"n/a"
                  },
                  "workClassName":{
                     "id":"workClassName",
                     "name":"班別名稱",
                     "value":"日常班",
                     "type":"string",
                     "format":"n/a"
                  },
                  "workOn":{
                     "id":"workOn",
                     "name":"上班時間",
                     "value":"0900",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "workOff":{
                     "id":"workOff",
                     "name":"下班時間",
                     "value":"1800",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "punchIn":{
                     "id":"punchIn",
                     "name":"進卡時間",
                     "value":"0854",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "punchOut":{
                     "id":"punchOut",
                     "name":"出卡時間",
                     "value":"1802",
                     "type":"string",
                     "format":"HHmm"
                  },
                  "isAbnormal":{
                     "id":"isAbnormal",
                     "name":"是否考勤異常",
                     "value":true,
                     "type":"boolean",
                     "format":"n/a"
                  },
                  "abnormal":{
                     "id":"abnormal",
                     "name":"考勤異常說明",
                     "value":"遲到1分鐘",
                     "type":"string",
                     "format":"n/a"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "board":{
         "id":"publishBoardInfo",
         "name":"公告資訊",
         "value":[
            {
               "id":"235",
               "name":"公告資料",
               "value":{
                  "seriesNo":{
                     "id":"seriesNo",
                     "name":"公告序號",
                     "value":"235",
                     "type":"string",
                     "format":"n/a"
                  },
                  "subject":{
                     "id":"subject",
                     "name":"公告主旨",
                     "value":"哈哈哈哈公告主旨",
                     "type":"string",
                     "format":"n/a"
                  },
                  "article":{
                     "id":"subject",
                     "name":"公告內文",
                     "value":"XXXXXXX",
                     "type":"string",
                     "format":"n/a"
                  },
                  "picture":{
                     "id":"picture",
                     "name":"公告圖片",
                     "value":"base64url",
                     "type":"string",
                     "format":"n/a"
                  },
                  "publisher":{
                     "id":"publisher",
                     "name":"公告人員工號",
                     "value":"L100387",
                     "type":"string",
                     "format":"n/a"
                  },
                  "publisherName":{
                     "id":"publisherName",
                     "name":"公告人員名稱",
                     "value":"林奇杰",
                     "type":"string",
                     "format":"n/a"
                  },
                  "publishDate":{
                     "id":"publishDate",
                     "name":"公告日期",
                     "value":"20211015",
                     "type":"string",
                     "format":"YYYYmmdd"
                  },
                  "publishTime":{
                     "id":"publishTime",
                     "name":"公告時間",
                     "value":"1802",
                     "type":"string",
                     "format":"HHmm"
                  }
               },
               "type":"object",
               "format":"n/a"
            }
         ],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{
            "YYYYmm":"西元年月",
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分",
	    "base64":"Base64資料庫格式",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when Failed
```json
{
    "status": "fail",
    "code": 406,
    "message": [
        "系統錯誤"
    ],
    "data": {}
}
```
