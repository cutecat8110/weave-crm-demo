# CRM

![Nuxt](https://img.shields.io/badge/Nuxt-v4-00DC82)
![Vue.js](https://img.shields.io/badge/Vue.js-v3-42b883)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6)
![Element Plus](https://img.shields.io/badge/Element_Plus-409EFF)

> 會員分級、聯絡歷程與對話搜尋，支援圖片預覽及中英切換。

![會員查詢與分級](images/members.png)

## 📋 專案概述

以會員為中心整合分級、福利與聯絡歷程，並將對話關聯至會員資料。支援顧問資料範圍、關鍵字命中定位，以及中英文介面切換。

**[開啟 Demo](https://cutecat8110.github.io/weave-crm-demo/#/login)**

## 功能入口

| 入口 | 代表操作 |
| --- | --- |
| [會員管理](https://cutecat8110.github.io/weave-crm-demo/#/members) | 多條件查詢、編修、福利資格與顧問資料範圍 |
| [會員分級](https://cutecat8110.github.io/weave-crm-demo/#/tiers) | 福利設定、啟停用及關聯檢查 |
| [聯絡紀錄](https://cutecat8110.github.io/weave-crm-demo/#/contacts) | 新增紀錄、安排追蹤與回看歷程 |
| [對話紀錄](https://cutecat8110.github.io/weave-crm-demo/#/conversations) | 分類、會員關聯、命中定位與圖片放大 |

## 🔨 核心技術

| 技術 | 用途 |
| --- | --- |
| Nuxt 4 / Vue 3 | 頁面、導覽與共用元件 |
| TypeScript | 會員與對話資料模型 |
| IndexedDB | 資料交易與版本檢查 |

## 🛠️ 擴展套件

| 技術 | 用途 |
| --- | --- |
| Element Plus | 查詢表單、表格與彈窗 |
| Element Plus Icons | 操作與狀態圖示 |

<details>
<summary>對話搜尋與聯絡歷程</summary>

![對話搜尋與圖片訊息](images/conversations.png)
![聯絡紀錄與追蹤狀態](images/contacts.png)

</details>

<details>
<summary>實作重點</summary>

共用查詢、表單與語系字典；對話搜尋保留前後文。IndexedDB 交易與版本檢查避免跨分頁覆蓋，儲存失敗保留草稿。

</details>

<details>
<summary>角色與使用說明</summary>

**試用：** 帶入管理員帳密 → 開啟林沐禾對話 → 搜尋「活動報名」→ 切換命中與查看圖片。右上角可切換中英介面。

管理員處理全部資料；顧問僅處理負責會員及相關紀錄；唯讀可查詢與匯出。

品牌、人物、對話及圖片均供展示。角色與福利由瀏覽器模擬，沒有訊息發送或伺服器身分驗證。修改保存在目前瀏覽器，中英切換不翻譯資料內容。

「重設資料」清除本作品各分頁的修改與草稿，恢復初始內容並登出；其他作品不受影響。

</details>
