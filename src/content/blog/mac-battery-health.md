---
title: "MacBook Pro 電池健康狀況檢查小技巧"
pubDate: 'Jan 15 2023'
description: ""
tags: ["mac","macbook","battery"]
heroImage: "https://images.unsplash.com/photo-1583863788434-e58a36330cf0?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1074&q=80"
# images is optional, but needed for showing Twitter Card
images: []
categories:
comment: true
draft: false
---

## MacBook Pro 電池健康情況查詢

2018 年 9 月入手的 Macbook Pro 13,
檢查了一下電池🔋的損耗情況。

## 檢查方法

1. 打開终端（Terminal）應用程式。
2. 在 terminal 輸入下方指令：

    ```bash
    ioreg -rn AppleSmartBattery | grep -i capacity

    ```

3. 執行指令後，你會看到類似以下結果的輸出：

    ```bash
        # 2023-01-15T22:18:36+08:00
        "AppleRawCurrentCapacity" = 4364
        "AppleRawMaxCapacity" = 4373
        "MaxCapacity" = 4373
        "CurrentCapacity" = 4364
        "DesignCapacity" = 5088

        "Cycle Count" = 163
    ```

在這個輸出中，你可以看到以下資訊：

- DesignCapacity：設計的最大電池容量，這裡的數值為 5088。
- MaxCapacity：電池的實際容量，這裡的數值為 4373。
- Cycle Count：電池已經循環的次數，這裡的數值為 163。

通過這些數值，你可以了解你的電池健康狀況。測試一下你的 MacBook 電池狀況吧！

