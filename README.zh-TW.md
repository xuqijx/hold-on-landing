[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [日本語](README.ja.md)

# Hold On（先別買）— 登陸頁

**Hold On（先別買）** 是一款 iOS 應用構想的靜態登陸頁：在衝動購物前加一段冷靜期。應用程式**尚未發布**，App Store 上還沒有；登陸頁目前用於收集搶先體驗的電子郵件。

線上網址：https://xuqijx.github.io/hold-on-landing/

## 規劃中的功能

1. **分享商品**：從購物 App 把商品分享到 Hold On。
2. **依價格冷靜**：等待時間隨價格增加，越貴等越久。
3. **稍後決定**：時間到後選擇購買或放棄，並看到省下多少。

頁面標示的規劃定價：$9.99 一次性解鎖，無訂閱，無廣告。

## 目錄結構

- `index.html` — Hold On 登陸頁，含「上線時通知我」電子郵件表單（Formspree）。
- `packs/` — 獨立的數位資料包銷售頁（給自由工作者的範本／工具包），入口 `/packs/`，購買按鈕連到 Gumroad。詳見 `packs/README.md`。
- `guides/` — 長文指南（如衝動消費冷靜期、固定價專案範圍蔓延），入口 `/guides/`。
- `favicon.ico`、`favicon-32.png` — 網站圖示。
- `robots.txt`、`sitemap.xml`。

## 本機執行

不需建置：

```bash
python3 -m http.server 8765
# 開啟 http://127.0.0.1:8765/
```

注意：圖示路徑使用 GitHub Pages 專案前綴 `/hold-on-landing/`，本機從根目錄存取時可能不顯示。

## 電子郵件表單

`index.html` 的表單提交到 Formspree（`https://formspree.io/f/xqppdwdw`）。若要自用，請替換表單的 `action`。請勿把收集到的郵件清單提交到本儲存庫。
