AI 旅遊保險智慧管家 V2.4.5.0 — 部署準備階段 1

注意：此檔案不是完成的 Vercel/Neon 部署版，請勿上傳 GitHub 或按 Deploy。

已完成：
1. 原始 ZIP 解包並保留程式與前端。
2. 移除測試 SQLite DB 檔，避免客戶／測試資料進 GitHub。
3. 加入 .gitignore、.env.example 與 Vercel 設定初稿。
4. Flask secret key 改為雲端必須設定 FLASK_SECRET_KEY；關閉預設 debug。

尚未完成：
1. SQLite 雙資料庫遷移 Neon PostgreSQL（同名 application_journey 表結構不同）。
2. INSERT OR REPLACE/IGNORE、PRAGMA、BEGIN IMMEDIATE 等 SQL 語法改造。
3. PostgreSQL 建表與 schema 隔離、持久化測試。
4. Vercel serverless 回歸測試及安全審查。

正式部署前需先完成上述項目；切勿直接將此階段版部署至 Vercel。
