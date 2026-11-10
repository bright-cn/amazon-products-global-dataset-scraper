# Amazon 全球商品数据集抓取工具

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-FF9A00?style=flat-square)](https://www.bright.cn/) [![爬虫工具 API](https://img.shields.io/badge/Scraper%20API-Available-FF9A00?style=flat-square)](https://www.bright.cn/products/web-scraper/amazon) [![数据集](https://img.shields.io/badge/Dataset-Available-0066CC?style=flat-square)](https://www.bright.cn/products/datasets/amazon) [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![许可证：MIT](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)

[![推广](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/products/web-scraper/amazon)

> **由 [Bright Data](https://www.bright.cn/) 提供支持的亚马逊全球商品数据集。**

本仓库提供两种大规模访问亚马逊全球商品数据集的方法：

- **[方法 1：Bright Data 亚马逊全球商品数据集爬虫工具 API](#方法-1bright-data-亚马逊全球商品数据集爬虫工具-api)**（推荐）- 完全托管的企业级爬虫 API，可自动处理代理、验证码和规模扩展。
- **[方法 2：Bright Data 亚马逊全球商品数据集](#方法-2bright-data-亚马逊全球商品数据集)** - 可直接下载的预采集亚马逊全球商品数据集，无需抓取。

## 目录

- [为什么使用 Bright Data 抓取亚马逊全球商品数据集？](#为什么使用-bright-data-抓取亚马逊全球商品数据集)
- [方法 1：Bright Data 亚马逊全球商品数据集爬虫工具 API](#方法-1bright-data-亚马逊全球商品数据集爬虫工具-api)
  - [快速开始](#开始使用亚马逊全球商品数据集爬虫工具-api)
  - [1. 亚马逊全球商品数据](#1-亚马逊全球商品数据)
- [方法 2：Bright Data 亚马逊全球商品数据集](#方法-2bright-data-亚马逊全球商品数据集)
- [数据采集方式](#数据采集方式)

## 为什么使用 Bright Data 抓取亚马逊全球商品数据集？

抓取亚马逊全球商品数据集面临多项挑战：

- 请求频率限制：亚马逊全球商品数据集会监控请求频率，并可能封禁超出限制的 IP。
- 验证码检测：自动访问可能会触发验证码挑战。
- 身份验证障碍：部分数据需要登录才能访问，且平台会检测自动化尝试。
- 动态内容加载：使用简单的 HTTP 请求很难抓取由 JavaScript 渲染的内容。
- IP 封禁：从同一 IP 重复发送请求可能会导致封禁。

Bright Data 的亚马逊全球商品数据集爬虫工具 API 通过以下功能解决这些问题：

- ✅ **内置动态代理**：自动绕过基于 IP 的请求频率限制
- ✅ **验证码破解**：无需任何额外设置即可应对机器人检测
- ✅ **结构化数据输出**：获取可直接用于分析的整洁 JSON
- ✅ **无需基础设施**：支持任意规模的云端托管抓取
- ✅ **99.9% 可用性 SLA**：为业务关键型工作流提供可靠的数据采集

## 方法 1：Bright Data 亚马逊全球商品数据集爬虫工具 API

[Bright Data 亚马逊全球商品数据集爬虫工具 API](https://www.bright.cn/products/web-scraper/amazon) 是一种完全托管的解决方案，无需设置任何基础设施。

### 开始使用亚马逊全球商品数据集爬虫工具 API

1. **注册**一个[免费的 Bright Data 账户](https://www.bright.cn/)
2. **前往**[亚马逊全球商品数据集爬虫工具 API](https://www.bright.cn/products/web-scraper/amazon)
3. 从控制面板**获取 API 令牌**
4. **安装** `requests` 库：`pip install requests`
5. **运行** `amazon-products-global-dataset_scraper_api_codes/` 中的任意脚本

### 1. 亚马逊全球商品数据

从亚马逊全球商品数据集采集全球商品数据。

#### 输入参数

| 字段 | 类型 | 必填 | 说明 |
|-------|------|----------|-------------|
| `url` | 字符串 | 是 | 要抓取的亚马逊全球商品数据集条目的 URL |
| `limit` | 整数 | 否 | 要返回的最大结果数量 |
| `include_errors` | 布尔值 | 否 | 在响应中包含错误详情 |
| `notify` | URL | 否 | 数据采集完成时用于接收通知的 Webhook URL |
| `format` | 枚举 | 否 | 输出格式：`JSON`、`NDJSON`、`JSON Lines`、`CSV` |

#### 响应示例

```json
{
  "answered_questions": 0,
  "asin": "B0BSHF7LLL",
  "availability": "Only 1 left in stock - order soon.",
  "brand": "Apple",
  "buybox_prices": {
    "final_price": 2693.79
  },
  "buybox_seller": "6ave",
  "climate_pledge_friendly": true,
  "currency": "USD",
  "date_first_available": "January 17, 2023",
  "delivery": [
    "FREE delivery Tuesday, April 28. "
  ],
  "description": "About this item SUPERCHARGED BY M2 PRO OR M2 MAX \u2014 Take on demanding projects with the M2 Pro or M2 Max chip. M2 Pro has 12 CPU cores, 19 GPU cores, and up to 32GB unified memory. M2 Max has 12 CPU cores, up to 38 GPU cores, and up to 96GB unified memory. UP TO 22 HOURS OF BATTERY LIFE \u2014 Go all day thanks to the power-efficient design of the M2 Pro or M2 Max chip. And the MacBook Pro laptop delivers exceptional performance whether it\u2019s running on battery or plugged in. FULLY COMPATIBLE \u2014 All your pro apps run lightning fast \u2014 including Adobe Creative Cloud, Xcode, Affinity Designer, Microsoft 365, and many of your favorite iPhone and iPad apps. BEAUTIFUL PRO DISPLAY \u2014 The 16.2-inch Liquid Retina XDR display features Extreme Dynamic Range, over 1000 nits of brightness for stunning HDR content, and pro reference modes for doing your best work on the go. ADVANCED CAMERA AND AUDIO \u2014 Look sharp and sound great with a 1080p FaceTime HD camera, a studio-quality three-mic array, and a six-speaker sound system with Spatial Audio. CONNECT WHAT YOU WANT \u2014 MacBook Pro features a MagSafe charging port, three Thunderbolt 4 ports, an SDXC card slot, an HDMI port, and a headphone jack. And enjoy seamless wireless connectivity with Wi-Fi 6E and Bluetooth 5.3. MAGIC KEYBOARD WITH TOUCH ID \u2014 Magic Keyboard comes with a full-height function key row and Touch ID, which gives you a fast, easy, secure way to unlock your Mac and sign in to apps and sites. WORKS WITH ALL YOUR APPLE DEVICES \u2014 You can do amazing things when you use your Apple devices together. Copy something on iPhone and paste it on MacBook Pro. Use your MacBook Pro to answer FaceTime calls or send texts with Messages. And that\u2019s just the beginning. BUILT TO LAST \u2014 The all-aluminum unibody enclosure is exceptionally durable. Free software updates keep things running smoothly and securely for years to come. LEGAL DISCLAIMERS \u2014 This is a summary of the main product features. See legal disclaimers below. Show more \u203a See more product details",
  "description_html": "About this item                     SUPERCHARGED BY M2 PRO OR M2 MAX \u2014 Take on demanding projects with the M2 Pro or M2 Max chip. M2 Pro has 12 CPU cores, 19 GPU cores, and up to 32GB unified memory. M2 Max has 12 CPU cores, up to 38 GPU cores, and up to 96GB unified memory.     UP TO 22 HOURS OF BATTERY LIFE \u2014 Go all day thanks to the power-efficient design of the M2 Pro or M2 Max chip. And the MacBook Pro laptop delivers exceptional performance whether it\u2019s running on battery or plugged in.     FULLY COMPATIBLE \u2014 All your pro apps run lightning fast \u2014 including Adobe Creative Cloud, Xcode, Affinity Designer, Microsoft 365, and many of your favorite iPhone and iPad apps.     BEAUTIFUL PRO DISPLAY \u2014 The 16.2-inch Liquid Retina XDR display features Extreme Dynamic Range, over 1000 nits of brightness for stunning HDR content, and pro reference modes for doing your best work on the go.     ADVANCED CAMERA AND AUDIO \u2014 Look sharp and sound great with a 1080p FaceTime HD camera, a studio-quality three-mic array, and a six-speaker sound system with Spatial Audio.     CONNECT WHAT YOU WANT \u2014 MacBook Pro features a MagSafe charging port, three Thunderbolt 4 ports, an SDXC card slot, an HDMI port, and a headphone jack. And enjoy seamless wireless connectivity with Wi-Fi 6E and Bluetooth 5.3.     MAGIC KEYBOARD WITH TOUCH ID \u2014 Magic Keyboard comes with a full-height function key row and Touch ID, which gives you a fast, easy, secure way to unlock your Mac and sign in to apps and sites.       \n                           WORKS WITH ALL YOUR APPLE DEVICES \u2014 You can do amazing things when you use your Apple devices together. Copy something on iPhone and paste it on MacBook Pro. Use your MacBook Pro to answer FaceTime calls or send texts with Messages. And that\u2019s just the beginning.  BUILT TO LAST \u2014 The all-aluminum unibody enclosure is exceptionally durable. Free software updates keep things running smoothly and securely for years to come.  LEGAL DISCLAIMERS \u2014 This is a summary of the main product features. See legal disclaimers below.      Show more            \u203a  See more product details",
  "domain": "https://www.amazon.com/",
  "fba_sellers_count": 0,
  "fbm_sellers_count": 0,
  "features": [
    "SUPERCHARGED BY M2 PRO OR M2 MAX \u2014 Take on demanding projects with the M2 Pro or M2 Max chip. M2 Pro has 12 CPU cores, 19 GPU cores, and up to 32GB unified memory. M2 Max has 12 CPU cores, up to 38 GPU cores, and up to 96GB unified memory.",
    "UP TO 22 HOURS OF BATTERY LIFE \u2014 Go all day thanks to the power-efficient design of the M2 Pro or M2 Max chip. And the MacBook Pro laptop delivers exceptional performance whether it\u2019s running on battery or plugged in.",
    "FULLY COMPATIBLE \u2014 All your pro apps run lightning fast \u2014 including Adobe Creative Cloud, Xcode, Affinity Designer, Microsoft 365, and many of your favorite iPhone and iPad apps.",
    "BEAUTIFUL PRO DISPLAY \u2014 The 16.2-inch Liquid Retina XDR display features Extreme Dynamic Range, over 1000 nits of brightness for stunning HDR content, and pro reference modes for doing your best work on the go.",
    "ADVANCED CAMERA AND AUDIO \u2014 Look sharp and sound great with a 1080p FaceTime HD camera, a studio-quality three-mic array, and a six-speaker sound system with Spatial Audio.",
    "CONNECT WHAT YOU WANT \u2014 MacBook Pro features a MagSafe charging port, three Thunderbolt 4 ports, an SDXC card slot, an HDMI port, and a headphone jack. And enjoy seamless wireless connectivity with Wi-Fi 6E and Bluetooth 5.3.",
    "MAGIC KEYBOARD WITH TOUCH ID \u2014 Magic Keyboard comes with a full-height function key row and Touch ID, which gives you a fast, easy, secure way to unlock your Mac and sign in to apps and sites.",
    "WORKS WITH ALL YOUR APPLE DEVICES \u2014 You can do amazing things when you use your Apple devices together. Copy something on iPhone and paste it on MacBook Pro. Use your MacBook Pro to answer FaceTime calls or send texts with Messages. And that\u2019s just the beginning.",
    "BUILT TO LAST \u2014 The all-aluminum unibody enclosure is exceptionally durable. Free software updates keep things running smoothly and securely for years to come.",
    "LEGAL DISCLAIMERS \u2014 This is a summary of the main product features. See legal disclaimers below."
  ],
  "final_price": 2693.79,
  "image_url": "https://m.media-amazon.com/images/I/61bwiPRcv2L._AC_SL1500_.jpg",
  "images": [
    "https://m.media-amazon.com/images/I/61bwiPRcv2L._AC_SL1500_.jpg",
    "https://m.media-amazon.com/images/I/71-uDe4TN1L._AC_SL1500_.jpg",
    "https://m.media-amazon.com/images/I/61C9irOOQVL._AC_SL1500_.jpg",
    "https://m.media-amazon.com/images/I/81KJXaswhrL._AC_SL1500_.jpg",
    "https://m.media-amazon.com/images/I/81OBjqVEGwL._AC_SL1500_.jpg",
    "https://m.media-amazon.com/images/I/61CdlgWgngL._AC_SL1500_.jpg",
    "https://m.media-amazon.com/images/I/61EXF2Vr9LL._AC_SL1500_.jpg"
  ],
  "images_count": 7,
  "initial_price": 2693.79,
  "input_asin": "B0BSHF7WHW",
  "is_amazon_as_seller": false,
  "is_available": true,
  "item_weight": "4.73 pounds",
  "manufacturer": "Apple",
  "model_number": "MNWC3LL/A",
  "number_of_sellers": 1,
  "parent_asin": "B0BSMHLDXD",
  "plus_content": false,
  "product_details": [
    {
      "type": "Product Dimensions",
      "value": "14.01 x 9.77 x 0.66 inches"
    },
    {
      "type": "Item Weight",
      "value": "4.73 pounds"
    },
    {
      "type": "Manufacturer",
      "value": "Apple"
    },
    {
      "type": "ASIN",
      "value": "B0BSHF7LLL"
    },
    {
      "type": "Item model number",
      "value": "MNWC3LL/A"
    },
    {
      "type": "Batteries",
      "value": "1 Lithium Ion batteries required. (included)"
    },
    {
      "type": "Date First Available",
      "value": "January 17, 2023"
    },
    {
      "type": "Brand",
      "value": "Apple"
    },
    {
      "type": "Model Name",
      "value": "MacBook Pro"
    },
    {
      "type": "Screen Size",
      "value": "16.2 Inches"
    },
    {
      "type": "Color",
      "value": "Silver"
    },
    {
      "type": "Hard Disk Size",
      "value": "512 GB"
    },
    {
      "type": "CPU Model",
      "value": "Unknown"
    },
    {
      "type": "Ram Memory Installed Size",
      "value": "16 GB"
    },
    {
      "type": "Operating System",
      "value": "Mac OS"
    },
    {
      "type": "Special Feature",
      "value": "Anti Glare Coating"
    },
    {
      "type": "Graphics Card Description",
      "value": "Integrated"
    }
  ],
  "product_dimensions": "14.01 x 9.77 x 0.66 inches",
  "product_rating_object": {
    "five_star": 421,
    "four_star": 34,
    "one_star": 10,
    "three_star": 15,
    "two_star": 5
  },
  "rating": 4.7,
  "reviews_count": 484,
  "seller_id": "ALAQLAKJ574UN",
  "seller_name": "6ave",
  "seller_url": "https://www.amazon.com/sp?ie=UTF8\u0026seller=ALAQLAKJ574UN\u0026asin=B0BSHF7LLL",
  "sponsered": false,
  "store_url": "https://www.amazon.com/stores/Apple/page/77D9E1F7-0337-4282-9DB6-B6B8FB2DC98D?lp_asin=B0BSHF7LLL\u0026ref_=ast_bln",
  "sustainability_features": [
    {
      "description": "Conserves energy compared to similar products.  EPEAT",
      "links": null,
      "title": "Energy efficiency"
    }
  ],
  "title": "Apple 2023 MacBook Pro Laptop with Apple M2 Pro chip with 12\u2011core CPU and 19\u2011core GPU: 16.2-inch Liquid Retina XDR Display, 16GB Unified Memory, 512GB SSD Storage. Works with iPhone/iPad; Silver",
  "top_review": "I upgraded from the $3,499 i9 Intel MacBook Pro from 2019, and this laptop seriously blows that away. The keyboard is amazing and so much better, the screen is amazing, I love the refresh rate, the responsiveness of jumping between pages and apps is so ridiculously fast, the trackpad and speakers are still just amazing, and the battery life on this is mind-blowing.Seriously, 10/10, absolutely recommend this to anyone, this thing is insane. I put it in my backpack for 9 days, and 9 days later it was still at 54%, even though it was powered on the entire time. I literally got a FaceTime call on my iPhone and my MacBook rang in my backpack at the same time on day 9.Get this MacBook if you need power and battery life, nothing will beat this.",
  "unit_price": {
    "price": 2693.79,
    "unit": null
  },
  "url": "https://www.amazon.com/dp/B0BSHF7LLL?th=1\u0026psc=1",
  "variations": [
    {
      "asin": "B0BSHF7LLL",
      "currency": null,
      "name": "Apple M2 Pro Chip Silver 512 GB",
      "price": null,
      "unit": null,
      "unit_price": null
    }
  ],
  "video": false,
  "video_count": 0
}
```

👉 查看[完整 Python 代码](amazon-products-global-dataset_scraper_api_codes/amazon_products_global_dataset_scraper.py)

## 方法 2：Bright Data 亚马逊全球商品数据集

如果你需要无需编写任何抓取代码即可使用的数据，[Bright Data 亚马逊全球商品数据集](https://www.bright.cn/products/datasets/amazon)提供预采集且定期更新的数据，可立即下载。

**为什么使用数据集而不是 API？**

- 📦 **即时访问**：无需设置、无需代码，也无需等待数据采集
- 🔄 **定期更新**：按固定计划刷新最新数据
- 📊 **多种格式**：支持下载为 JSON、JSONL 或 CSV
- 🌍 **超大规模**：涵盖亚马逊全球商品数据集所有主要类别的数百万条记录
- ✅ **完全合规**：以合乎道德的方式获取，并通过法律合规审查

👉 **[探索亚马逊全球商品数据集](https://www.bright.cn/products/datasets/amazon)**

## 数据采集方式

| 功能 | Bright Data 爬虫工具 API | Bright Data 数据集 |
|---------|------------------------|---------------------|
| 所需设置 | 仅需 API 令牌 | 无需设置 |
| 实时数据 | ✅ 是 | ❌ 预采集 |
| 自定义查询 | ✅ 完全控制 | ❌ 固定模式 |
| 包含代理 | ✅ 内置动态代理 | N/A |
| 验证码破解 | ✅ 自动 | N/A |
| 规模 | 无限 | 无限 |
| 结构化输出 | ✅ JSON / NDJSON / JSON Lines / CSV | ✅ JSON / JSONL / CSV |
| 支持 | 企业级 24/7 支持 | 企业级 24/7 支持 |

---

🔗 **了解更多**：[https://www.bright.cn/products/web-scraper/amazon](https://www.bright.cn/products/web-scraper/amazon)
