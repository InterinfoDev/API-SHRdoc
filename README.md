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

## Program list
### 登入

| 功能名稱        | API名稱               | 功能說明                               |
|-----------------|-----------------------|----------------------------------------|
| 登入            | appLogin              | 驗證使用者帳號密碼                     |

### 登出

| 功能名稱        | API名稱               | 功能說明                               |
|-----------------|-----------------------|----------------------------------------|
| 登出            | appLogout             | 記錄使用者登出資訊                     |

### 共用元件

| 功能名稱        | API名稱               | 功能說明                               |
|-----------------|-----------------------|----------------------------------------|
| 登出            | appLogout             | 記錄使用者登出資訊                     |
| 登入            | appLogin              | 驗證使用者帳號密碼                     |
| 功能元件        | appAgentQuery         | 取得代理人清單                         |
| 功能元件        | appAllDepartment      | 取得目前有在使用的全部部門             |
| 功能元件        | appCompanySuper       | 取得某員工公司別可視範圍資料           |
| 功能元件        | appDeptCondition      | 取得某員工可視部門資料                 |
| 功能元件        | appEmployeeCondition  | 取得某員工可視範圍員工資料             |
| 功能元件        | appEmployeePhoto      | 取得特定員工照片資訊                   |
| 功能元件        | appFlowHistory        | 取得該筆單據流程紀錄                   |
| 功能元件        | appGenerateQRCode     | 產生登入qrCode                         |
| 功能元件        | appGoogleMapKey       | 取得GoogleMap使用Key                   |
| 功能元件        | appNonEmployeeCondition| 取得全部員工資料                      |
| 功能元件        | appPinCode            | 驗證識別碼取得設定資訊                 |
| 功能元件        | appPushSetting        | 查詢通知設定                           |
| 功能元件        | appQueryAgentFunction | 取得代理簽核的下拉選項                 |
| 功能元件        | appQueryHkind         | 取得查詢條件假別的下拉選項             |
| 功能元件        | appSetting            | 取得設定資料                           |
| 功能元件        | appSignFlow           | 取得簽核畫面核准或退簽按鈕所回傳的資訊 |
| 功能元件        | appTranslate          | 取得裝置端翻譯後訊息                   |
| 功能元件        | appVerifyQRCode       | 驗證QRCODE資訊                         |

### 大聲公

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 大聲公         | appAnnouncement           | 查詢通知訊息資訊                       |
| 大聲公         | appAnnouncementLatest     | 查詢通知新訊息資訊                     |
| 大聲公         | appAnnouncementNotify     | 取得未讀取通知數量                     |
| 大聲公         | appAnnouncementQuery      | 查詢特定通知訊息資訊                   |

## 互動打卡

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 互動打卡       | appBeaconPunchCard        | Beacon打卡                             |
| 互動打卡       | appBeaconSetting          | 取得Beacon打卡資訊                     |

## 公告訊息

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 公告訊息       | appBoardList              | 取得公告清單資訊                       |
| 公告訊息       | appBoardQuery             | 取得公告詳細資訊                       |

### 文件下載

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 文件下載       | appDownloadFile           | 檔案下載                               |
| 文件下載       | appPaperList              | 取得文件下載清單                       |

### 出差變更

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 出差變更       | appTravelChangeAdd        | 員工出差變更                           |
| 出差變更       | appTravelChangeApply      | 新增出差時程變更申請單畫面所需要的資訊 |
| 出差變更       | appTravelChangeDetail     | 查詢該出差變更單詳細資料               |
| 出差變更       | appTravelChangeField      | 出差變更單申請畫面欄位                 |
| 出差變更       | appTravelChangeList       | 查詢單一員工該年月區間的出差變更資訊   |
| 出差變更       | appTravelChangeMonth      | 查詢員工出差變更資訊                   |
| 出差變更       | appTravelChangeVerifyField| 出差變更畫面欄位檢核                   |

### 加班異常

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 加班異常       | appIrregularOvertimeApply | 加班異常欄位預設值                     |
| 加班異常       | appIrregularOvertimeExec  | 異動加班異常                           |
| 加班異常       | appIrregularOvertimeList  | 取得加班異常列表資訊                   |
| 加班異常       | appIrregularOvertimeMail  | 加班異常寄信                           |
| 加班異常       | appIrregularOvertimeMailRecord | 取得加班異常信件通知紀錄            |
| 加班異常       | appIrregularOvertimeMonth | 取得加班異常資訊                       |
| 加班異常       | appIrregularOvertimePDF   | 取得員工加班異常名單PDF                |
| 加班異常       | appIrregularOvertimeViewType | 取得查詢條件顯示種類的下拉選項       |

### 未結案單據

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 未結案單據     | appCaseDetail             | 未結案詳細資料                         |

### 生物辨識

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 生物辨識       | appMemoryPwd              | 生物辨識記憶密碼驗證員工登入密碼       |
| 生物辨識       | appMemorySalaryPwd        | 生物辨識記憶密碼驗證員工薪資條密碼     |

## 考勤打卡

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 考勤打卡       | appGpsPunchCard           | GPS線上打卡                            |
| 考勤打卡       | appGpsSetting             | 取得GPS打卡資訊                        |
| 考勤打卡       | appWorkPlace              | 取得使用者上班地點資訊                 |

### 考勤報表

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 考勤報表       | appAttendDetail           | 取得指定年月、員工考勤詳細資料         |
| 考勤報表       | appAttendList             | 取得考勤列表資訊                       |
| 考勤報表       | appAttendMonth            | 取得員工指定某年月考勤資訊             |

### 考勤補卡

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 考勤補卡       | appQueryReason            | 取得補卡原因的下拉選項                 |
| 考勤補卡       | appSupplementaryApply     | 取得補卡資訊與當天班別資訊             |
| 考勤補卡       | appSupplementaryCardAdd   | 員工考勤補卡                           |
| 考勤補卡       | appSupplementaryCardDetail| 查詢該補假詳細資料                     |
| 考勤補卡       | appSupplementaryCardList  | 查詢單一員工該年月區間的補卡資訊       |
| 考勤補卡       | appSupplementaryCardMonth | 取得員工補卡資訊                       |

### 行事曆

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 行事曆         | appDeleteEmployeeCalendar | 刪除員工行事曆                         |
| 行事曆         | appEditEmployeeCalendar   | 異動員工個人行事曆                     |
| 行事曆         | appEmployeeCalendarList   | 取得特定員工行事曆資訊                 |
| 行事曆         | appEmployeeCalendarQuery  | 取得員工個人行事曆特定事件詳細資料     |

### 忘記密碼

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 忘記密碼       | appForgotPwd              | 執行忘記密碼                           |

### 事後加班

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 事後加班       | appAfterwardsOvertimeApply| 新增事後加班單畫面所需要的資訊         |
| 事後加班       | appAfterwardsOvertimeField| 事後加班單申請畫面欄位                 |

### 待簽核單據

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 待簽核單據     | appFlowList               | 取得使用者待簽核單據詳細資料           |
| 待簽核單據     | appFlowNotify             | 取得簽核單據數量                       |
| 待簽核單據     | appFlowTodoList           | 取得使用者待簽核單據                   |

## 首頁資訊

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 首頁資訊       | appHomePage               | 取得首頁資訊                           |

### 個人獎金

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 個人獎金       | appSalbondIndate          | 取得員工指定年月獎金入帳日期資訊       |
| 個人獎金       | appSalbondQuery           | 取得指定年月、員工獎金條明細資訊       |
| 個人獎金       | appSalbondRecent          | 取得某員工最近一次獎金發放資訊         |

### 個人薪資

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 個人薪資       | appSalaryCompanySuper     | 取得某員工公司別可視薪資範圍資料       |
| 個人薪資       | appSalaryCount            | 發薪次數資訊                           |
| 個人薪資       | appSalaryPwd              | 驗證員工薪資條密碼(獎金通用)           |
| 個人薪資       | appSalaryQuery            | 取得指定年月、員工薪資條明細資訊       |
| 個人薪資       | appSalaryRecent           | 取得某員工最近一次薪資發放資訊         |

### 員工出差

| 功能名稱       | API名稱                   | 功能說明                               |
|----------------|---------------------------|----------------------------------------|
| 員工出差       | appTravelAdd              | 員工出差                               |
| 員工出差       | appTravelVerifyField      | 出差單畫面欄位檢核                     |
| 員工出差       | appTravelDetail           | 查詢該出差單詳細資料                   |
| 員工出差       | appTravelField            | 出差單申請畫面欄位                     |
