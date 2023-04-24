# appFlowList
取得使用者待簽核單據詳細資料

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appFlowList
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
| request | {key:xxx} | Object | 查詢條件

### JSON representation
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "key":"635144642219404571194688689683105522531368129784502001284860188282814076207411"
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
| key | 635144642219404571194688689683105522531368129784502001284860188282814076207411 | String | 鍵值 | Y | n/a |


### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "flowList":{
         "name":"CA7.人事異動單簽核-待簽核列表",
         "type":"array",
         "value":[
            {
               "name":"No.4",
               "type":"object",
               "value":{
                  "fields":{
                     "name":"欄位資訊",
                     "type":"array",
                     "value":[
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"W00201908210001",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"單據編號",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"1276",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"員工編號",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"聶O倫",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"員工姓名",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"調任",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"異動項目",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"test",
                              "format":"n/a",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請說明",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20190826",
                              "format":"YYYYmmdd",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"生效日期",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"20190821",
                              "format":"YYYYmmdd",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請日期",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        },
                        {
                           "fieldValue":{
                              "name":"欄位資料",
                              "type":"string",
                              "value":"111841",
                              "format":"HHmmss",
                              "id":"fieldValue"
                           },
                           "fieldName":{
                              "name":"欄位名稱",
                              "type":"string",
                              "value":"申請時間",
                              "format":"n/a",
                              "id":"fieldName"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"fields"
                  },
                  "keys":{
                     "name":"欄位鍵值",
                     "type":"array",
                     "value":[
                        {
                           "uniqueValue":{
                              "name":"鍵值資料",
                              "type":"string",
                              "value":"W00201908210001",
                              "format":"n/a",
                              "id":"uniqueValue"
                           },
                           "uniqueField":{
                              "name":"鍵值名稱",
                              "type":"string",
                              "value":"102466946499809093666",
                              "format":"n/a",
                              "id":"uniqueField"
                           }
                        }
                     ],
                     "format":"n/a",
                     "id":"keys"
                  },
                  "signFlow":{
                     "name":"簽核資訊",
                     "type":"object",
                     "value":{
                        "approveUrl":{
                           "name":"簽核網址",
                           "type":"string",
                           "value":"http://114.34.125.246:8090/servlet/jform?file=hrm8w.pkg&init_func=CA7.人事異動單簽核&locale=TW&uid=admin&pwd=EM.SESSION.625050713326173689562490441831943248094599718872274406774617189206105869712493&em_flowkey=W00201908210001",
                           "format":"hyperlink",
                           "id":"approveUrl"
                        }
                     },
                     "format":"n/a",
                     "id":"signFlow"
                  }
               },
               "format":"n/a",
               "id":"3"
            }
         ],
         "format":"n/a",
         "id":"flowList"
      },
      "flowButton":{
         "name":"簽核按鈕",
         "type":"object",
         "value":{
            "reject":{
               "name":"退簽",
               "type":"object",
               "value":{
                  "buttonName":{
                     "name":"按鈕名稱",
                     "type":"string",
                     "value":"退簽",
                     "format":"n/a",
                     "id":"buttonName"
                  },
                  "buttonKey":{
                     "name":"按鈕代碼",
                     "type":"string",
                     "value":"[退簽]",
                     "format":"n/a",
                     "id":"buttonKey"
                  },
                  "visible":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"visible"
                  }
               },
               "format":"n/a",
               "id":"reject"
            },
            "approve":{
               "name":"核准",
               "type":"object",
               "value":{
                  "buttonName":{
                     "name":"按鈕名稱",
                     "type":"string",
                     "value":"核准",
                     "format":"n/a",
                     "id":"buttonName"
                  },
                  "buttonKey":{
                     "name":"按鈕代碼",
                     "type":"string",
                     "value":"核准",
                     "format":"n/a",
                     "id":"buttonKey"
                  },
                  "visible":{
                     "name":"是否顯示",
                     "type":"boolean",
                     "value":true,
                     "format":"n/a",
                     "id":"visible"
                  }
               },
               "format":"n/a",
               "id":"approve"
            }
         },
         "format":"n/a",
         "id":"flowButton"
      },
      "properties":{
         "format":{
            "YYYYmmdd":"西元年月日",
            "n/a":"",
            "HHmmss":"時間時分秒",
            "hyperlink":"超連結"
         }
      }
   }
}
```

### HTTP Response when No Data 
```json
{
    "status": "success",
    "message": [
        "您已無待簽核單據"
    ],
    "data": {
        "properties": {
            "format": {
                "n/a": "",
                "hyperlink": "超連結"
            }
        },
        "flowList": {
            "name": "CB2.12.出差時程變更單簽核-待簽核列表",
            "type": "array",
            "value": [],
            "format": "n/a",
            "id": "flowList"
        },
        "flowButton": {
            "name": "流程按鈕",
            "type": "object",
            "value": {
                "reject": {
                    "name": "退簽",
                    "type": "object",
                    "value": {
                        "buttonName": {
                            "name": "按鈕名稱",
                            "type": "string",
                            "value": "退簽",
                            "format": "n/a",
                            "id": "buttonName"
                        },
                        "buttonKey": {
                            "name": "按鈕代碼",
                            "type": "string",
                            "value": "[退簽]",
                            "format": "n/a",
                            "id": "buttonKey"
                        },
                        "visible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "visible"
                        }
                    },
                    "format": "n/a",
                    "id": "reject"
                },
                "approve": {
                    "name": "核准",
                    "type": "object",
                    "value": {
                        "buttonName": {
                            "name": "按鈕名稱",
                            "type": "string",
                            "value": "核准",
                            "format": "n/a",
                            "id": "buttonName"
                        },
                        "buttonKey": {
                            "name": "按鈕代碼",
                            "type": "string",
                            "value": "核准",
                            "format": "n/a",
                            "id": "buttonKey"
                        },
                        "visible": {
                            "name": "是否顯示",
                            "type": "boolean",
                            "value": true,
                            "format": "n/a",
                            "id": "visible"
                        }
                    },
                    "format": "n/a",
                    "id": "approve"
                }
            },
            "format": "n/a",
            "id": "flowButton"
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
