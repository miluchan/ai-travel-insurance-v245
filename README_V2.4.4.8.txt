V2.4.4.8｜已繳費即時鎖定修正版
- DB 查詢/投保明細既已正確，本版只修前端畫面沒有即時切換到 PAID 的問題。
- 付款成功後立即設定前端 PAYMENT_COMPLETED，付款按鈕改為「已繳費」並停用。
- 選「暫時不要」後直接移除付款與核保面板，只保留「已繳費、暫不出單」提示。
- goPaymentFromUW 增加前端 PAID guard，不可再開付款畫面。
- pay-demo 後端增加重複付款 guard：PAID/PAYMENT_COMPLETED/POLICY_CREATED/CLOSED 一律拒絕再次付款。
- 不修改已正確的投保查詢與投保明細資料。
