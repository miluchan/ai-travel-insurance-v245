V2.4.4.7｜已繳費狀態與被保險人資料交易修正版
- 修正空白「暫時不要」按鈕：改為明確可見文字按鈕。
- Demo付款改走既有 /api/v21/application/<jid>/pay-demo，等待DB成功寫入 PAYMENT_COMPLETED/PAID 後才顯示出單選擇。
- 不再用 legacy saveJourney 假性更新付款狀態，因此投保查詢會正確顯示「已繳費」，且不會再出現可重複付款。
- 核保改走既有 V2R underwriting/check；只有 person_profile 已真正寫入 DB 才能進入核保/付款。
- 被保險人仍沿用既有 confirm-persons transaction 寫入 person_profile；付款前由後端 checkpoint 強制驗證，避免畫面有資料但DB沒有資料。
- 已繳費案件不可刪除；執行顯示「確定出單」。
