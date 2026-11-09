# 北京奧利兔音樂節 FOH 單曲試聽頁（aolitu-foh-aod）

## 目的
把北京奧利兔音樂節 2026-09-12 橘隊 FOH 演出錄音的十首單曲（BlendVision AOD）整理成一頁公開網頁，
列出曲名與展示間短網址，給組織外的人（樂手、客戶）不登入就能打開試聽。可加到手機主畫面。
做法比照 h14-hours-app：GitHub Pages 靜態頁。claude.ai Artifact 因組織關閉對外分享而不採用。

## 範圍鐵則
- 純靜態：index.html + manifest.webmanifest + 圖示，無後端、無金鑰、不打 BlendVision API。
- 曲目資料只在 index.html 的 `ROWS` 常數；換連結或加曲只改這裡。
- 頁面帶 `noindex`，不讓搜尋引擎收錄；但 repo 與網址本身是公開的，知道網址的人都能開。
- 短網址來自 bv_upload.py 的 share_link（冪等，同一支 AOD 永遠回同一條）。AOD 被刪，連結就失效。

## 退場條件
不再對外分享這批錄音時：關 GitHub Pages、repo 封存或刪除。BlendVision 端的 AOD 另行處理。

## 產出歸屬
- 正式網址：https://hsiao-tzu.github.io/aolitu-foh-aod/
- 原始檔：NAS prod_③_dev_jane/reh/Sessions/Archive/北京奧莉兔_show20260912.tar 內的 Bounced Files。
