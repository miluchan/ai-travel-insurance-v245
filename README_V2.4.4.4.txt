V2.4.4.4｜Premium API 我要投保銜接修正版
問題根因：
- Premium API 已完成方案選擇與正式試算，但 directPremiumApplication 建立 quote 時只有 product.company/name，
  沒有舊 checkpoint2 所要求的 product.id / product_code，因此後端誤判「尚未選定投保商品」。

修正：
- Premium API 三方案建立穩定 product_code：
  PREMIUM-ECONOMY / PREMIUM-BALANCED / PREMIUM-ENHANCED。
- quote 同時帶 product_code/product_name/insurer_name/total_premium。
- checkpoint2 對 premium_api quote 增加安全 fallback。
- 不恢復舊 Demo 商品搜尋頁；按「我要投保」仍直接銜接既有投保資料助手。
