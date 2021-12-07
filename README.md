# HRNative-Document
HR Native Web API Document
提供 iOS / Android Web 互動 API

### HTTP Request
```
https://114.34.125.246:8090/servlet/HRNative/appAttendDetail
```

### HTTP Request Mehod
```
POST
```

### Query Filter Style
公司別下拉選單

| Current Field | Display Field | Current Value | Display Value |
|:----------|:----------|:----------|:----------|
| companyId | companySimpleName | 97090920  | 英特內軟體 |

部門下拉選單

| Current Field | Display Field | Current Value | Display Value | 
|:----------|:----------|:----------|:----------|
| depNumber | depCode + ' ' + depFullName | 10  | C3200 研發處 |

員工下拉選單

| Current Field | Display Field | Current Value | Display Value | 
|:----------|:----------|:----------|:----------|
| empid | empid + ' ' + empName | L100387  | L100387 林奇杰 |

發薪次數下拉選單

| Current Field | Display Field | Current Value | Display Value | 
|:----------|:----------|:----------|:----------|
| countInfo | countInfo | 1  | 1 |

### Program list
| Program Senario | Program Name | ReadyToUse | Description | Author | Last Modify Date |
|:----------|:----------|:----------|:----------|:----------|:----------|
| 考勤詳細 | appAttendDetail | N | 取得指定年月、員工考勤詳細資料 |  |  |
| 考勤列表 | appAttendList | Y | 取得考勤列表資訊 | AndyHou | 20211202 |
| 年月考勤 | appAttendMonth | Y | 取得員工指定某年月考勤資訊 | AndyHou | 20211202 |
| 公司別權限 | appCompanySuper | Y | 取得某員工公司別可視範圍資料 | AndyHou | 20211202 |
| 夥伴查詢 | appContact | Y | 取得夥伴查詢資料 | Kevin | 20211202 |
| 部門權限 | appDeptCondition | Y | 取得某員工可視部門資料 | AndyHou | 20211202 |
| 特定員工行事曆 | appEmployeeCalendarList | Y | 取得特定員工行事曆資訊 | Kevin | 20211206 |
| 個人行事曆詳細 | appEmployeeCalendarQuery | Y | 取得員工個人行事曆特定事件詳細資料 | Kevin | 20211206 |
| 異動行事曆 | appEditEmployeeCalendar | Y | 取得員工個人行事曆特定事件詳細資料 | Kevin | 20211206 |
| 員工權限 | appEmployeeCondition | Y | 取得某員工可視範圍員工資料 | AndyHou | 20211202 |
| 員工照片 | appEmployeePhoto | Y | 取得特定員工照片資訊 | AndyHou | 20211202 |
| 忘記密碼 | appForgotPwd | N | 執行忘記密碼 |  |  |
| APP功能權限 | appFunctionRight | Y | 取得員工APP功能資訊 | Danielweng | 20211207 |
| 線上打卡 | appGpsPunchCardGPS | Y | 線上打卡 | AndyHou | 20211202 | 
| 取得首頁 | appHomePage | Y | 取得首頁資訊 | AndyHou | 20211202 |
| 驗證帳號密碼 | appLogin | Y | 驗證使用者帳號密碼 | AndyHou | 20211203 |
| 發薪次數 | appSalaryCount | Y | 發薪次數資訊 | Kevin | 20211202 |
| 驗證薪資條密碼 | appSalaryPwd | Y | 驗證員工薪資條密碼(獎金通用) | Kevin | 20211202 |
| 薪資條明細 | appSalaryQuery | Y | 取得指定年月、員工薪資條明細資訊 | Daniel | 20211203 |
| 最近一次薪資發放 | appSalaryRecent | Y | 取得某員工最近一次薪資發放資訊 | Daniel | 20211203 |
| 獎金條明細 | appSalbondQuery | N | 取得指定年月、員工獎金條明細資訊 | Daniel | 20211206 |
| 最近一次獎金發放 | appSalbondRecent | N | 取得某員工最近一次獎金發放資訊 | Daniel | 20211206 |
| 體溫回報 | appBodyTemperature | Y | 提供使用者回報體溫資訊 | AndyHou | 20211202 |
| GoogleMap | appGoogleMapKey | N | 提供GoogleMapKey資訊 | AndyHou | 20211205 |
