### 我把一家多通路電商的營運，做成了會自己跑的系統

一人開發，8 支無人值守的排程 agent 每天在跑真實營運工作——產圖、建檔、盤點、補貨、對帳。
使用者是公司裡的設計師與採購同仁，**每個工作天都在用，壞了會有人來問**。

> I build the automation that runs a multi-channel e-commerce operation.
> 8 unattended scheduled agents, in production, used by colleagues every working day.

---

| | |
| :-- | --: |
| 無人值守的排程 agent · Unattended agents in production | **8 支** |
| 上架圖產出 · Listing images shipped | **1,045 張** |
| 自動建檔進 ERP · SKUs auto-created in ERP | **69** |
| 產線管理的品項 · SKUs under management | **244** |
| 測試覆蓋 · Test coverage | 產線 **62%** ／ 工具鏈 **49%** |
| 上線至今 · In production since | 2026-07 |

---

### 我實際在做的事

**設計會停下來等人的自動化。** 全自動很誘人，但有些判斷機器做不對——版面的品味、例外的處置。所以我的產線在關鍵處留人工關卡，其餘全自動。難的不是決定要不要留，是**決定留在哪一步**。

**假設系統會安靜地騙我。** 跑完沒報錯不等於做對了；排程沒動作可能是正確閒置，也可能是排程器已經不再觸發它。這兩者在日誌上長得一模一樣，而**分不出來的監控等於沒有監控**。上線至今累積了 176 則失敗模式紀錄，多數是「它回報成功，但什麼都沒做」。

**用 AI coding 工具寫、也用它驗。** 我為 Google Apps Script 手寫了測試替身與 fixture——因為假替身只要比真 API 寬鬆一點，測試就會在真正出事的地方給你綠燈。

---

### 精選作品

**[design-ops-pipeline](https://github.com/JL226/design-ops-pipeline)** — 一條無人值守的商品圖產線，中間留了一道設計師確認關卡
架構、六條決策紀錄、上線後才學到的四件事，以及那個花兩週才想通的問題：**放行的勾選欄，語意到底是「請出圖」還是「已確認」。**

---

### 工具

`Python` · `Google Apps Script` · `Claude Code` · `Codex` · 排程 agent · 瀏覽器自動化 · Google Workspace API · 電商 ERP 整合

<sub>Taiwan · 電商共同創辦人，自己寫自己用的系統</sub>
