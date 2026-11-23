V2.4.4.2 AI規劃保障流程修正
根因：
1. AI規劃按鈕誤呼叫不存在的舊函式 v217RequireInsurancePeriod。
2. 套用方案預設勾選後又執行 sync/getPlan sync，導致後端舊 profile 把勾選狀態覆蓋。
修正：
- 統一使用 v2402RequireInsurancePeriod，並檢核啟程/回程日期與時間。
- AI規劃流程改為：先同步表單→判斷方案→套用預設→同步→再次固定預設→顯示方案。
- getPlan 不再先 sync 覆蓋勾選。
- 預算較低：班機延誤、行李延誤、行李損失。
- 基本/提高：上述3項＋旅程取消＋旅程更改（API codes 488/490）。
