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


### Calendar List Style
行事曆列表有資料時顯示
<dl>
  <dt>樣式一</dt>
  <dd>2021/12/01 ~ 2021/12/31 全天</dd>

  <dt>樣式二</dt>
  <dd>2021/12/01 全天</dd>

  <dt>樣式三</dt>
  <dd>2021/12/01 09:00 ~ 18:00</dd>

  <dt>樣式四</dt>
  <dd>2021/12/01 09:00 ~ 2021/12/31 18:00</dd>
</dl>

### Program list
| Program Senario | Program Name | ReadyToUse | Description | Author | Last Modify Date |
|:----------|:----------|:----------|:----------|:----------|:----------|
| 考勤詳細 | appAttendDetail | Y | 取得指定年月、員工考勤詳細資料 | Daniel | 20211217 |
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
| 忘記密碼 | appForgotPwd | N | 執行忘記密碼 | Kevin | 20211203 |
| APP功能權限 | appFunctionRight | Y | 取得員工APP功能資訊 | Daniel | 20211207 |
| 線上打卡 | appGpsPunchCardGPS | Y | 線上打卡 | AndyHou | 20211202 | 
| 取得首頁 | appHomePage | Y | 取得首頁資訊 | AndyHou | 20211202 |
| 驗證帳號密碼 | appLogin | Y | 驗證使用者帳號密碼 | AndyHou | 20211203 |
| 發薪次數 | appSalaryCount | Y | 發薪次數資訊 | Kevin | 20211202 |
| 驗證薪資條密碼 | appSalaryPwd | Y | 驗證員工薪資條密碼(獎金通用) | Kevin | 20211202 |
| 薪資條明細 | appSalaryQuery | Y | 取得指定年月、員工薪資條明細資訊 | Daniel | 20211203 |
| 最近一次薪資發放 | appSalaryRecent | Y | 取得某員工最近一次薪資發放資訊 | Daniel | 20211203 |
| 獎金條明細 | appSalbondQuery | Y | 取得指定年月、員工獎金條明細資訊 | Daniel | 20211206 |
| 最近一次獎金發放 | appSalbondRecent | Y | 取得某員工最近一次獎金發放資訊 | Daniel | 20211206 |
| 體溫回報 | appBodyTemperature | Y | 提供使用者回報體溫資訊 | AndyHou | 20211202 |
| GoogleMap | appGoogleMapKey | Y | 提供GoogleMapKey資訊 | AndyHou | 20211205 |
| 量測體溫介面裝置資訊 | appTemperatureInterface | N | 提供量測體溫介面裝置資訊 | AndyHou | 20211222 |
| 個人資料維護欄位 | appPersonalColumnMaintenance | N | 取得維護欄位 | AndyHou | 20220124 |
| 個人資料維護異動 | appPersonalDataMaintenance | N | 異動個人資料 | AndyHou | 20220124 |
| 下載檔案 | appDownloadFile | N | 取得下載檔案 | AndyHou | 20220106 |
| 請假單詳細資料 | appVacationDetail | Y | 取得指定請假單詳細資料 | Kevin | 20220122 |
| 請假單列表 | appVacationList | Y | 取得請假列表資訊 | Kevin | 20220122 |
| 請假單年月 | appVacationMonth | Y | 取得員工指定某年月請假資訊 | Kevin | 20220122 |
| 待簽核單據 | appFlowTodoList | Y | 取得員工待簽核單據列表 | Lucas | 20220215 |
| 簽核詳細列表 | appFlowList | Y | 取得待簽核功能的詳細資料 | Lucas | 20220215 |
| 請假畫面資訊 | appVacationApply | Y | 取得請假畫面資訊 | Kevin | 20220221 |
| 流程簽核 | appSignFlow | Y | 簽核畫面按鈕程式 | Kevin | 20220321 |
| 預定加班單詳細資料 | appOverplanDetail | Y | 取得指定預定加班單詳細資料 | Kevin | 20220412 |
| 預定加班單列表 | appOverplanList | Y | 取得預定加班單列表資訊 | Kevin | 20220412 |
| 預定加班單年月 | appOverplanMonth | Y | 取得員工指定某年月預定加班資訊 | Kevin | 20220412 |
| 流程紀錄 | appFlowHistory | Y | 取得該筆單據流程紀錄 | Kevin | 20220412 |
| 通知訊息資訊 | appAnnouncement | N | 查詢通知訊息資訊 | AndyHou | 20220425 |
| 通知訊息數量 | appAnnouncementNotify | N | 取得未讀取通知數量 | AndyHou | 20220425 |
| 公告清單 | appBoardList | N | 取得公告資訊 | AndyHou | 20220425 |
| 公告資訊 | appBoardQuery | N | 取得公告資訊 | AndyHou | 20220425 |
| 移除裝置紀錄 | appDeviceDelete | N | 移除使用者裝置紀錄 | AndyHou | 20220425 |
| 裝置清單 | appDeviceList | N | 取得使用者裝置清單 | AndyHou | 20220425 |
| 紀錄裝置 | appDeviecRecord | N | 紀錄裝置識別碼 | AndyHou | 20220425 |
| 異動通知設定 | appExecPushSetting | N | 異動通知設定 | Richard | 20220425 |
| 通知設定 | appPushSetting | N | 查詢通知設定 | Richard | 20220425 |
| 簽核訊息數量 | appFlowNotify | N | 取得簽核通知數量 | AndyHou | 20220425 |
| 考勤打卡 | appGpsPunchCard | N | 異動考勤打卡資訊 | AndyHou | 20220425 |
| 登出帳號 | appLogout | N | 紀錄登出資訊 | AndyHou | 20220425 |
| 預定加班單資訊 | appOverplanApply | Y | 預定加班單資訊 | Kevin | 20220425 |
| 驗證識別碼 | appPinCode | N | 驗證識別碼取得設定資訊 | AndyHou | 20220425 |
| 假別清單 | appQueryHkind | N | 取得假別清單 | AndyHou | 20220425 |
| 補卡原因清單 | appQueryReason | N | 取得補卡原因清單 | AndyHou | 20220425 |
| 公司法規條文 | appRecognitionTerms | N | 取得使用者公司法規條文 | AndyHou | 20220425 |
| 獎金入帳日期 | appSalbondIndate | N | 取得員工指定年月獎金入帳日期 | AndyHou | 20220425 |
