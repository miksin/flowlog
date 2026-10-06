# 流水本

隨手記小筆記的單頁 web app。一個輸入框，Enter 送出，筆記按時間疊成流水；零依賴、零 build、存在瀏覽器裡，不出網路。

**功能**

- 單輸入框 + Enter 快記，新筆記螢光黃掃過提示
- 跨日自動分組（TODAY / YESTERDAY / 日期＋星期）
- 即時搜尋（`/` 快捷鍵聚焦，Esc 清除）
- 點筆記就地編輯，hover 刪除
- localStorage 持久化，PWA 可離線、可裝手機主畫面

**部屬**

純靜態檔案，丟上任何 server 即可（service worker 需 HTTPS 或 localhost）：

```bash
python3 -m http.server 8000
# → http://localhost:8000/
```

**還沒做的**（要用了再說）：#tag、todo 勾選、跨裝置同步（屆時資料只是 `{id, text, ts}` 陣列，升級rie 零遷移成本）。
