# appExecFlowAgent
異動簽核代理人

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appExecFlowAgent
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
| request | {empid:admin,agent:0169,functionCode:590535521097405056829363076749951101069612102461523530525384772277901512134546,dateType:C,startDate:20220519,endDate:20220520,startTime:1230,endTime:1800} | Object | 查詢條件

### JSON representation Case 1 - 永遠代理 (dateType = 空白)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "agent":"0169",
        "functionCode":"590535521097405056829363076749951101069612102461523530525384772277901512134546",
        "dateType":""
    }
}
```

### JSON representation Case 2 - 指定特定日期 (dateType = A)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "agent":"0169",
        "functionCode":"590535521097405056829363076749951101069612102461523530525384772277901512134546",
        "dateType":"A",
        "startDate":"20220519"
    }
}
```

### JSON representation Case 3 - 指定日期區間 (dateType = B)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "agent":"0169",
        "functionCode":"590535521097405056829363076749951101069612102461523530525384772277901512134546",
        "dateType":"B",
        "startDate":"20220519",
        "endDate":"20220520"
    }
}
```

### JSON representation Case 4 - 指定特定日期時間區間 (dateType = C)
Here is a JSON representation of request.
```json
{
    "uid":"98599308101484732326",
    "right":"51341911904173543336756162544864820",
    "request":{
        "empid":"admin",
        "agent":"0169",
        "functionCode":"590535521097405056829363076749951101069612102461523530525384772277901512134546",
        "dateType":"C",
        "startDate":"20220519",
        "endDate":"20220520",
        "startTime":"1230",
        "endTime":"1800"
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
| Key | Value | Type | Description | Required | Format | Note |
|:----------|:-------------|:-----|:------------|:------------|:------------|:------------|
| empid | admin | String | 被代理人 | N | n/a |  |
| agent | 0169 | String | 代理人 | N | n/a |  |
| functionCode | xxxxxx | String | 功能名稱 | N | n/a |  |
| dateType | A | boolean | 全天 | Y | n/a | 空白:永遠代理,A:指定特定日期,B:指定日期區間,C:指定特定日期時間區間 |
| startDate | 20220519 | String | 代理起始日期 | Y | DATE(YYYYmmdd) | 起始日期 |
| endDate | 20220520 | String | 代理結束日期 | Y | DATE(YYYYmmdd) | 結束日期 |
| startTime | 1230 | String | 代理起始時間 | Y | TIME(HHmm) | 起始時間 |
| endTime | 1800 | String | 代理結束時間 | Y | TIME(HHmm) | 結束時間 |

### HTTP Response when Successful
```json
{
   "status":"success",
   "message":[
      "回傳成功"
   ],
   "data":{
      "flowAgent":{
         "name":"異動簽核代理人",
         "type":"object",
         "value":{
            "executeMessage":{
               "name":"異動訊息",
               "type":"string",
               "value":"設定成功，因被代理人未設電子信箱，將不會收到通知",
               "format":"n/a",
               "id":"executeMessage"
            },
            "executeResult":{
               "name":"異動結果",
               "type":"boolean",
               "value":true,
               "format":"n/a",
               "id":"executeResult"
            }
         },
         "format":"n/a",
         "id":"flowAgent"
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
