# appHomePage
取得首頁資訊

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
| right | 51341911904173543336756162544864820 | String | 需透過appLogin取得 |
| request | {} | Object | 查詢條件 |


### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{ --取消empid傳入
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

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "personal":{
         "id":"personal", --lucas
         "name":"員工資訊",
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
            "depFullName":{ --lucas
               "id":"depFullName",
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
         "id":"attend", --lucas
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
                     "format":"YYYYmmdd" --lucas
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
         "id":"board", --lucas
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
                     "value":"base64",  --lucas
                     "type":"string",
                     "format":"base64"  --lucas
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
         "format":{ --lucas 拿掉YYYYmm
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分",
	    "base64":"Base64資料庫格式",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Board Data or Attend Data
Board 或 Attend 無資料，但Board無資料則隱藏該區塊，但整體來說不算是錯誤，正常來說可以不用有資料
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "personal":{
         "id":"personalInfo",
         "name":"個人資訊",
         "value":{"...":"..."},
         "type":"object",
         "format":"n/a"
      },
      "attend":{
         "id":"attendInfo",
         "name":"考勤資訊",
         "value":[],    --無資料則是顯示
         "type":"array",
         "format":"n/a"
      },
      "board":{
         "id":"publishBoardInfo",
         "name":"公告資訊",
         "value":[],
         "type":"array",
         "format":"n/a"
      },
      "properties":{
         "format":{ --lucas 拿掉YYYYmm
            "YYYYmmdd":"西元年月日",
            "HHmm":"時間時分",
	    "base64":"Base64資料庫格式",
            "n/a":""
         }
      }
   }
}
```

### HTTP Response when No Data
無資料則屬於 Code 500 錯誤，正常來說一般使用者一定會有Personal資料，若Personal無資料，則出錯。
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
