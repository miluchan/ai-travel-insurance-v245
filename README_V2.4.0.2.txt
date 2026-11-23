V2.4.0.2 修正版
修正「AI 幫我規劃保障」無反應：V2.4.0.1 誤呼叫不存在的 v217RequireInsurancePeriod。
本版改用自包含的 v2402RequireInsurancePeriod，檢查啟程日/回程日與日期先後。
已靜態驗證完整呼叫鏈：
plan button -> getPlan -> period guard -> sync -> 三方案 UI -> realPremiumBtn -> getRealPremium -> /api/premium/quote。
