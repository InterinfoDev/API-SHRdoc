# appTravelAdd
員工出差

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appTravelAdd
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
| request | {'empid':'admin','startDate':'20220628','endDate':'20220630','startTime':'1230','endTime':'1830','note':'AndyHou測試出差單備註','jobAgent':'0169','flowAgent':'0169','flowAgent1':'','flowAgent2':'','flowAgent3':'',"travelType":"A",'travelPlace':'台北南港','traffic':'4','contact':'測試-聯絡方式','currency':'USD','isHoliday':false,'people':'測試-出差人員及分工方式','visit':'測試-拜訪對象','schedule':'測試-行程規劃','point':'測試-訪談重點及預期效果','authorize':'測試-希望授權事項及幅度','assist':'測試-協助他部門辦理事項','preCost':300.0,'scheduleList':[{'startDate':'20220628','endDate':'20220630','days':'3','city':'台北'}],'scheduleFile':[{'fileName':'測試檔案.jpg','fileData':''}],'travelFile':[{'fileName':'測試檔案.jpg','fileData':''}]} | Object | 異動條件

### JSON representation Case 1
Here is a JSON representation of request.
```json
{
   "uid":"98599308101484732326",
   "right":"51341911904173543336756162544864820",
   "request":{
      "empid":"admin",
      "startDate":"20220628",
      "endDate":"20220630",
      "startTime":"1230",
      "endTime":"1830",
      "note":"AndyHou測試出差單備註",
      "jobAgent":"0169",
      "flowAgent":"0169",
      "flowAgent1":"",
      "flowAgent2":"",
      "flowAgent3":"",
      "travelType":"A",
      "travelPlace":"台北南港",
      "traffic":"4",
      "contact":"測試-聯絡方式",
      "currency":"USD",
      "people":"測試-出差人員及分工方式",
      "visit":"測試-拜訪對象",
      "schedule":"測試-行程規劃",
      "point":"測試-訪談重點及預期效果",
      "authorize":"測試-希望授權事項及幅度",
      "assist":"測試-協助他部門辦理事項",
      "preCost":300.0,
      "scheduleList":[
         {
            "startDate":"20220628",
            "endDate":"20220630",
            "days":"3",
            "city":"台北"
         }
      ],
      "scheduleFile":[
         {
            "fileName":"測試檔案1.jpg",
            "fileData":""
         }
      ],
      "travelFile":[
         {
            "fileName":"測試檔案2.jpg",
            "fileData":""
         }
      ]
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
| empid | admin | String | 員工編號 | Y | n/a |
| startDate | 20220628 | String | 起始日期 | Y | YYYYmmdd |
| endDate | 20220630 | String | 結束日期 | Y | YYYYmmdd |
| startTime | 1900 | String | 起始時間 | Y | HHmm |  
| endTime | 2300 | String | 結束時間 | Y | HHmm |         
| note | test | String | 備註 | N | n/a |
| jobAgent | 10900015 | String | 職務代理人 | Y | n/a | 
| flowAgent | 10900015 | String | 簽核代理人 | N | n/a | 
| flowAgent1 | 10900015 | String | 代理人一 | N | n/a | 
| flowAgent2 | 10900015 | String | 代理人二 | N | n/a | 
| flowAgent3 | 10900015 | String | 代理人三 | N | n/a | 
| travelType | A | String | 出差類別 | Y | n/a |
| travelPlace | 台北南港 | String | 出差地點 | Y | n/a |
| travelPlace | 4 | String | 交通方式 | Y | n/a |
| contact | 電話09xxxxxxxx | String | 聯絡方式 | N | n/a |
| currency | USD | String | 幣別代號 | N | n/a |
| people | 王小明 | String | 出差人員及分工方式 | N | n/a |
| visit | XX科技-課長 | String | 拜訪對象 | N | n/a |
| schedule | 行程內容 | String | 行程規劃 | N | n/a |
| point | 處理客戶問題(XXX) | String | 訪談重點及預期效果 | N | n/a |
| assist | 行動硬碟*1 | String | 協助他部門辦理事項 | N | n/a |
| preCost | 300.0 | Decimal | 預支旅費 | Y | n/a |
| scheduleList | startDate:起始日期,endDate:結束日期,startTime:起始時間,endTime:結束時間 | Object | 預定行程 | N | n/a |
| travelFile | fileName:測試檔案.jpg,fileData:base64 | Object | 出差附件 | N | n/a |
| scheduleFile | fileName:測試檔案.jpg,fileData:base64 | Object | 出差附件 | N | n/a |
| isHoliday | false | boolean | 是否包含假日 | N | n/a |

### HTTP Response when Successful
```json
{
    "status": "success",
    "message": [
        "回傳成功"
    ],
    "data": {
        "addTravel": {
            "name": "新增出差單",
            "type": "object",
            "value": {
                "executeMessage": {
                    "name": "異動訊息",
                    "type": "string",
                    "value": "本單(xxx)已完成確認，謝謝",
                    "format": "n/a",
                    "id": "executeMessage"
                },
                "executeResult": {
                    "name": "異動結果",
                    "type": "boolean",
                    "value": true,
                    "format": "n/a",
                    "id": "executeResult"
                }
            },
            "format": "n/a",
            "id": "addTravel"
        },
        "properties": {
            "format": {
                "n/a": ""
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
