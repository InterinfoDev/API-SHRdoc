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

| API名稱               | 功能說明                               |
|-----------------------|----------------------------------------|
| appAgentQuery         | 取得代理人清單                         |
| appAllDepartment      | 取得目前有在使用的全部部門             |
| appCompanySuper       | 取得某員工公司別可視範圍資料           |
| appDeptCondition      | 取得某員工可視部門資料                 |
| appEmployeeCondition  | 取得某員工可視範圍員工資料             |
| appEmployeePhoto      | 取得特定員工照片資訊                   |
| appFlowHistory        | 取得該筆單據流程紀錄                   |
| appGenerateQRCode     | 產生登入qrCode                         |
| appGoogleMapKey       | 取得GoogleMap使用Key                   |
| appNonEmployeeCondition| 取得全部員工資料                      |
| appPinCode            | 驗證識別碼取得設定資訊                 |
| appPushSetting        | 查詢通知設定                           |
| appQueryAgentFunction | 取得代理簽核的下拉選項                 |
| appQueryHkind         | 取得查詢條件假別的下拉選項             |
| appSetting            | 取得設定資料                           |
| appSignFlow           | 取得簽核畫面核准或退簽按鈕所回傳的資訊 |
| appTranslate          | 取得裝置端翻譯後訊息                   |
| appVerifyQRCode       | 驗證QRCODE資訊                         |

### 功能權限

| API名稱               | 功能說明                               |
|-----------------------|----------------------------------------|
| appFunctionRight      | 取得員工APP功能資訊                    |

### 大聲公

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appAnnouncement           | 查詢通知訊息資訊                       |
| appAnnouncementLatest     | 查詢通知新訊息資訊                     |
| appAnnouncementNotify     | 取得未讀取通知數量                     |
| appAnnouncementQuery      | 查詢特定通知訊息資訊                   |

### 互動打卡

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appBeaconPunchCard        | Beacon打卡                             |
| appBeaconSetting          | 取得Beacon打卡資訊                     |

### 公告訊息

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appBoardList              | 取得公告清單資訊                       |
| appBoardQuery             | 取得公告詳細資訊                       |

### 文件下載

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appDownloadFile           | 檔案下載                               |
| appPaperList              | 取得文件下載清單                       |

### 出差變更

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appTravelChangeAdd        | 員工出差變更                           |
| appTravelChangeApply      | 新增出差時程變更申請單畫面所需要的資訊 |
| appTravelChangeDetail     | 查詢該出差變更單詳細資料               |
| appTravelChangeField      | 出差變更單申請畫面欄位                 |
| appTravelChangeList       | 查詢單一員工該年月區間的出差變更資訊   |
| appTravelChangeMonth      | 查詢員工出差變更資訊                   |
| appTravelChangeVerifyField| 出差變更畫面欄位檢核                   |

### 加班異常

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appIrregularOvertimeApply | 加班異常欄位預設值                     |
| appIrregularOvertimeExec  | 異動加班異常                           |
| appIrregularOvertimeList  | 取得加班異常列表資訊                   |
| appIrregularOvertimeMail  | 加班異常寄信                           |
| appIrregularOvertimeMailRecord | 取得加班異常信件通知紀錄            |
| appIrregularOvertimeMonth | 取得加班異常資訊                       |
| appIrregularOvertimePDF   | 取得員工加班異常名單PDF                |
| appIrregularOvertimeViewType | 取得查詢條件顯示種類的下拉選項       |

### 未結案單據

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appCaseDetail             | 未結案詳細資料                         |

### 生物辨識

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appMemoryPwd              | 生物辨識記憶密碼驗證員工登入密碼       |
| appMemorySalaryPwd        | 生物辨識記憶密碼驗證員工薪資條密碼     |

### 考勤打卡

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appGpsPunchCard           | GPS線上打卡                            |
| appGpsSetting             | 取得GPS打卡資訊                        |
| appWorkPlace              | 取得使用者上班地點資訊                 |

### 考勤報表

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appAttendDetail           | 取得指定年月、員工考勤詳細資料         |
| appAttendList             | 取得考勤列表資訊                       |
| appAttendMonth            | 取得員工指定某年月考勤資訊             |

### 考勤補卡

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appQueryReason            | 取得補卡原因的下拉選項                 |
| appSupplementaryApply     | 取得補卡資訊與當天班別資訊             |
| appSupplementaryCardAdd   | 員工考勤補卡                           |
| appSupplementaryCardDetail| 查詢該補假詳細資料                     |
| appSupplementaryCardList  | 查詢單一員工該年月區間的補卡資訊       |
| appSupplementaryCardMonth | 取得員工補卡資訊                       |

### 行事曆

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appDeleteEmployeeCalendar | 刪除員工行事曆                         |
| appEditEmployeeCalendar   | 異動員工個人行事曆                     |
| appEmployeeCalendarList   | 取得特定員工行事曆資訊                 |
| appEmployeeCalendarQuery  | 取得員工個人行事曆特定事件詳細資料     |

### 忘記密碼

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appForgotPwd              | 執行忘記密碼                           |

### 事後加班

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appAfterwardsOvertimeApply| 新增事後加班單畫面所需要的資訊         |
| appAfterwardsOvertimeField| 事後加班單申請畫面欄位                 |

### 待簽核單據

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appFlowList               | 取得使用者待簽核單據詳細資料           |
| appFlowNotify             | 取得簽核單據數量                       |
| appFlowTodoList           | 取得使用者待簽核單據                   |

### 首頁資訊

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appHomePage               | 取得首頁資訊                           |

### 個人獎金

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appSalbondIndate          | 取得員工指定年月獎金入帳日期資訊       |
| appSalbondQuery           | 取得指定年月、員工獎金條明細資訊       |
| appSalbondRecent          | 取得某員工最近一次獎金發放資訊         |

### 個人薪資

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appSalaryCompanySuper     | 取得某員工公司別可視薪資範圍資料       |
| appSalaryCount            | 發薪次數資訊                           |
| appSalaryPwd              | 驗證員工薪資條密碼(獎金通用)           |
| appSalaryQuery            | 取得指定年月、員工薪資條明細資訊       |
| appSalaryRecent           | 取得某員工最近一次薪資發放資訊         |

### 員工出差

| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appTravelAdd              | 員工出差                               |
| appTravelVerifyField      | 出差單畫面欄位檢核                     |
| appTravelDetail           | 查詢該出差單詳細資料                   |
| appTravelField            | 出差單申請畫面欄位                     |
| appTravelList             | 查詢單一員工該年月區間的出差資訊       |
| appTravelMonth            | 查詢員工出差資訊                       |

### 員工請假

| API名稱                   | 功能說明                                                                                                                |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------|
| appVacationAdd			| 員工請假																 							        			  |
| appVacationApply			| 新增假別畫面所需要的所有資訊，包含請假者資訊，假別選項(含該假別使用情況)，以及特休和加班補休使用情況					  |
| appVacationDetail			| 查詢該假單詳細資料			                                                          								  |
| appVacationField			| 請假單申請畫面欄位																									  |
| appVacationInfo			| 取得所選假別使用情況																									  |
| appVacationList			| 查詢單一員工該年月區間的請假資訊																						  |
| appVacationMonth			| 查詢員工請假資訊																										  |
| appVacationVerifyField	| 請假畫面欄位檢核，之後若其他功能有需要用到欄位檢核也會依照此格式回傳，主要會傳入欲檢核的欄位名稱以及畫面上所有欄位的資料|

### 通知
| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appExecNotification	    | 更新推播資訊已讀						 |
| appNotificationDetail     | 取得推播詳細資料                       |
| appNotificationList       | 查詢推播清單                           |
| appNotificationListLatest | 查詢推播清單最新資訊(全部)             |
| appNotificationSearchList | 查詢搜尋頁推播資訊                     |
| appReadAll                | 已讀全部推播訊息                       |
| appReadNotification       | 取得未讀取鈴鐺通知數量                 |
| appRecognitionTerms       | 查詢使用者公司法規條文                 |
| appUnReadStatus           | 查詢各通知類別未讀取資訊               |

### 裝置紀錄
| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appDeviceList   			| 取得使用者裝置清單					 |
| appDeviceRecord			| 紀錄裝置識別碼           				 |

### 裝置綁定
| API名稱                   | 功能說明                               |
|---------------------------|----------------------------------------|
| appBindingStatus   		| 查詢綁定狀態					 		 |
| appBindingTerms			| 查詢綁定協議內容           			 |
| appDeleteBinding   		| 解除綁定								 |
| appDeviceDelete			| 移除裝置紀錄           				 |
| appExecBinding   			| 綁定裝置								 |

### 資料維護
| API名稱                     | 功能說明                               |
|-----------------------------|----------------------------------------|
| appContact   				  | 取得夥伴查詢資料					   |
| appPersonalColumnMaintenance| 個人資料維護欄位           			   |
| appPersonalDataMaintenance  | 個人資料維護異動					   |

### 預定加班
| API名稱                     | 功能說明                               |
|-----------------------------|----------------------------------------|
| appOverplanAdd              | 新增預定加班單                         |
| appOverplanApply            | 新增預定加班單畫面所需要的資訊         |
| appOverplanDetail           | 查詢該預定加班單詳細資料               |
| appOverplanField            | 預定加班單申請畫面欄位                 |
| appOverplanList             | 查詢單一員工該年月區間的預定加班資訊   |
| appOverplanMonth            | 查詢員工預定加班資訊                   |
| appOverplanVerifyField      | 預定加班單畫面欄位檢核                 |
																	   
### 實際加班
| API名稱                     | 功能說明                               |
|-----------------------------|----------------------------------------|
| appOvertimeAdd              | 新增實際加班單，新增事後加班單         |
| appOvertimeApply            | 新增實際加班單畫面所需要的資訊         |
| appOvertimeDetail           | 查詢該假單詳細資料                     |
| appOvertimeField            | 實際加班單申請畫面欄位                 |
| appOvertimeList             | 查詢單一員工該年月區間的實際加班資訊   |
| appOvertimeMonth            | 查詢員工實際加班資訊                   |
| appOvertimeVerifyField      | 實際加班單畫面欄位檢核                 |

### 噠噠
| API名稱                     | 功能說明                                      |
|-----------------------------|-----------------------------------------------|
| appChatCreateGroup          | 創建群組聊天室                                |
| appChatCreatePersonal       | 創建個人聊天室，或從夥伴查詢進入也是使用此API |
| appChatGroupList            | 群組聊天室資料列表                            |
| appChatGroupSend            | 群體傳送                                      |
| appChatLatestText           | 往上滑取得新的聊天紀錄                        |
| appChatPastText             | 往下滑取得舊的聊天紀錄                        |
| appChatPersonalList         | 個人聊天室列表資料                            |
| appChatRoom                 | 點及聊天室獲取該聊天室相關資料                |
| appChatSendText             | 發送訊息                                      |
| appChatTextReader           | 取得訊息讀取資料                              |
| appChatUnread               | 聊天室未讀訊息(群組+個人)                     |
| appOriginalImage            | 取得原始上傳圖片                              |

### 簽核代理
| API名稱                     | 功能說明                                      |
|-----------------------------|-----------------------------------------------|
| appExecFlowAgent            | 異動簽核代理人                                |
| appExpireFlowAgent          | 刪除簽核代理人資訊                            |
| appFlowAgentDetail          | 查詢單筆簽核代理人詳細資料                    |
| appFlowAgentList            | 查詢簽核代理人資訊                            |

### 體溫回報
| API名稱                     | 功能說明                                      |
|-----------------------------|-----------------------------------------------|
| appBodyTemperature          | 回報當日體溫                                  |
| appTemperatureInterface     | 查詢體溫裝置介面                              |

