[English](README.md) | [简体中文](README.zh-CN.md) | [繁體中文](README.zh-TW.md) | [日本語](README.ja.md)

# Hold On（先别买）— 落地页

**Hold On（先别买）** 是一款 iOS 应用构想的静态落地页：在冲动购物前加一段冷静期。应用**尚未发布**，App Store 上还没有；落地页目前用于收集抢先体验邮箱。

线上地址：https://xuqijx.github.io/hold-on-landing/

## 计划中的功能

1. **分享商品**：从购物 App 把商品分享到 Hold On。
2. **按价格冷静**：等待时长随价格增加，越贵等越久。
3. **稍后决定**：时间到后选择购买或放弃，并看到省下了多少。

页面标注的计划定价：$9.99 一次性解锁，无订阅，无广告。

## 目录结构

- `index.html` — Hold On 落地页，含“上线时通知我”邮箱表单（Formspree）。
- `packs/` — 独立的数字资料包销售页（面向自由职业者的模板/工具包），入口 `/packs/`，购买按钮跳转 Gumroad。详见 `packs/README.md`。
- `guides/` — 长文指南（如冲动消费冷静期、固定价项目范围蔓延），入口 `/guides/`。
- `favicon.ico`、`favicon-32.png` — 网站图标。
- `robots.txt`、`sitemap.xml`。

## 本地运行

无需构建：

```bash
python3 -m http.server 8765
# 打开 http://127.0.0.1:8765/
```

注意：图标路径使用 GitHub Pages 项目前缀 `/hold-on-landing/`，本地从根目录访问时可能不显示。

## 邮箱表单

`index.html` 中的表单提交到 Formspree（`https://formspree.io/f/xqppdwdw`）。如需自用，替换表单的 `action`。请勿把收集到的邮箱列表提交到本仓库。
