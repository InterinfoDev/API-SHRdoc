# appPaperList
取得文件下載清單

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appPaperList
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

### JSON representation

```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
}
```

### Properties
| Property | Type | Description |
|:---------|:-----|:------------|
| uid   | String | 加密後帳號 |
| right | String | 加密後系統相關資料 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "paperList":{
         "name":"文件清單",
         "type":"object",
         "value":[
            {
               "files":{
                  "name":"文件檔案",
                  "type":"array",
                  "value":[
                     {
                        "fileType":{
                           "name":"檔案類型",
                           "type":"string",
                           "value":"image/jpeg",
                           "format":"n/a",
                           "id":"fileType"
                        },
                        "fileUrl":{
                           "name":"檔案路徑",
                           "type":"string",
                           "value":"68003594272853068328337346134317287570913311845073470440016105690972866842246009293386519267298844711625895434880013085613046014921492674893766088396318112",
                           "format":"n/a",
                           "id":"fileUrl"
                        },
                        "fileName":{
                           "name":"檔案名稱",
                           "type":"string",
                           "value":"1652156973268_1652087661461.jpg",
                           "format":"n/a",
                           "id":"fileName"
                        }
                     }
                  ],
                  "format":"n/a",
                  "id":"files"
               },
               "paperNo":{
                  "name":"文件編號",
                  "type":"string",
                  "value":"0720150001",
                  "format":"n/a",
                  "id":"paperNo"
               },
               "paperName":{
                  "name":"文件名稱",
                  "type":"string",
                  "value":"文件管理",
                  "format":"n/a",
                  "id":"paperName"
               },
               "validStartDate":{
                  "name":"有效起日",
                  "type":"string",
                  "value":"20150621",
                  "format":"YYYYmmdd",
                  "id":"validStartDate"
               },
               "uploader":{
                  "name":"上傳人員",
                  "type":"string",
                  "value":"池O祥",
                  "format":"n/a",
                  "id":"uploader"
               },
               "isDownload":{
                  "name":"是否可以下載",
                  "type":"boolean",
                  "value":true,
                  "format":"n/a",
                  "id":"isDownload"
               },
               "depFullName":{
                  "name":"單位名稱",
                  "type":"string",
                  "value":"L1線A班",
                  "format":"n/a",
                  "id":"depFullName"
               },
               "announcePlace":{
                  "name":"發表位置",
                  "type":"string",
                  "value":"對外公開",
                  "format":"n/a",
                  "id":"announcePlace"
               },
               "validEndDate":{
                  "name":"有效迄日",
                  "type":"string",
                  "value":"20990630",
                  "format":"YYYYmmdd",
                  "id":"validEndDate"
               }
            },
            {
               "files":{
                  "name":"文件檔案",
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
                           "value":"5723330362703420542532656963749592958003640236232535008240350599902758399057216867876751649889940233629423282301070030919068696836149885103459562606129279559656558339542074495684249233516608113328151796808290594498025645192990659461820590884498775575428777981658596747770915151170683698404111246033534184832335004316830272030109783031138564375490064949255327078328057",
                           "format":"n/a",
                           "id":"fileUrl"
                        },
                        "fileName":{
                           "name":"檔案名稱",
                           "type":"string",
                           "value":"1652156990241_[V8客製(福隆)_ M.4.10.2.生產獎金結算作業._hrm8d_nag.dat-Baron-20220506-技術處]+ 當月應出勤總時數.docx",
                           "format":"n/a",
                           "id":"fileName"
                        }
                     }
                  ],
                  "format":"n/a",
                  "id":"files"
               },
               "paperNo":{
                  "name":"文件編號",
                  "type":"string",
                  "value":"C20130001",
                  "format":"n/a",
                  "id":"paperNo"
               },
               "paperName":{
                  "name":"文件名稱",
                  "type":"string",
                  "value":"管理類",
                  "format":"n/a",
                  "id":"paperName"
               },
               "validStartDate":{
                  "name":"有效起日",
                  "type":"string",
                  "value":"20130620",
                  "format":"YYYYmmdd",
                  "id":"validStartDate"
               },
               "uploader":{
                  "name":"上傳人員",
                  "type":"string",
                  "value":"卓O伶",
                  "format":"n/a",
                  "id":"uploader"
               },
               "isDownload":{
                  "name":"是否可以下載",
                  "type":"boolean",
                  "value":true,
                  "format":"n/a",
                  "id":"isDownload"
               },
               "depFullName":{
                  "name":"單位名稱",
                  "type":"string",
                  "value":"",
                  "format":"n/a",
                  "id":"depFullName"
               },
               "announcePlace":{
                  "name":"發表位置",
                  "type":"string",
                  "value":"對外公開",
                  "format":"n/a",
                  "id":"announcePlace"
               },
               "validEndDate":{
                  "name":"有效迄日",
                  "type":"string",
                  "value":"20991231",
                  "format":"YYYYmmdd",
                  "id":"validEndDate"
               }
            }
         ],
         "format":"n/a",
         "id":"paperList"
      },
      "properties":{
         "format":{
            "n/a":""
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
