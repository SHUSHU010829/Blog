---
title: "怎麼解決 Xcode 在開啟專案時超久的問題"
date: 2023-04-17T14:34:51+08:00
description: "How to solved xcode continues project loading forever problem?"
draft: false
weight: false
aliases: default
summary: "解決 Xcode 轉圈地獄。"
tags: "iOS", "Xcode"
categories: default
author: "Shu"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
hidemeta: false
comments: true
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
cover:
    # image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

## 前言

在 App 專案開發時，真的很常為了開啟一個專案而費時超久，久到系統直接判定"毫無反應"。我的時間都花在上面了啦！！
剛開始還以為是個人電腦問題，就任命的等待。有一天在我重啟 Xcode 十次後真的實在受不了去找找解決方法後，意外發現解決方法超級簡單，所以分享給各位。

## 原來是 iCloud 搞的鬼！

在嘗試了一堆刪除資料夾等等的做法但一無用處後，突然看到了一個把 iCloud 同步關掉就可以解決這問題的回覆，保持著不要錯過的精神也做嘗試了，但他給的回覆是去設定直接把整台同步關閉，但有很多專案我還是想同步至 iCloud 去做儲存，所以找到了超級簡單的解決方法。

### 把個別資料夾標記不與同步就好啦

把不想同步的資料夾後面添加 **.nosync**。
例如: "project1" -> "project1.nosync"

就可以使個別資料夾不同步上傳，這時再次用 Xcode 打開它，只需幾秒鐘就開啟了！（感天動地TAT）

## 參考連結
[How to stop iCloud from syncing a folder?](https://cntechpost.com/2020/03/28/how-to-stop-icloud-from-syncing-a-folder/#:~:text=For%20example%2C%20project%20files%20such,folders%20continuously%20uploaded%20and%20unavailable.&text=At%20this%20point%20you%20just,nosync%22%20to%20the%20file%20name.)
