---
layout:     post
title:      "Good Team, Good Work"
subtitle:   "strive"
date:       2017-10-08 12:00:00
author:     "ilake"
header-img: "img/post-bg-weekly.jpg"
tags:
    - life
---

# good team, good work

> 之前和朋友聊天, 聊到一些開發團隊, 很容易會遇到的幾個問題
>
> 因此想在這邊分享一下看法以及過去經驗裡實際運用的解法

有討論到的幾個問題分別是

> 1. sprint 會議的問題
2. 對於 bug 沒有危機意識
3. 如何開始 devops
4. 如何加快團隊步調
5. 沒有 ownership

### 1. sprint 會議的問題
> 沒有效率, 沒有檢討會議, 沒有後續追蹤


目前 sprint meeting 沒有效率, 發生的情況是:
>
> * 沒有人負責且知道大家手上有哪些事情
> * 會議上所有人同時浪費很多時間在看 ticket, 想解法

我覺得這邊有幾個需要改善的點

1. RD resource 不明, leader 需要掌握 RD resource
2. 需要 leader 與 PM 的 Sprint Planning Meet
3. retrospective meeting 要持續 並且有後續追蹤 不然沒意義

leader 需要能掌握大家目前手上的事情, 至少也必須在 Sprint Planning Meet 確認幾件事情

> * 分析票 確實知道票要做什麼
* 確認哪些票是要放在這個 sprint
* sprint meeting 和大家變成只是分配工作

> 如此一來 leader 也可掌握每個人手頭上的工作, 臨時插單也會知道是誰來處理
>
> 之後的 spring meeting 大家再根據接到的任務 自己看需不需要切小票
>
> * 每日 stand up meeting 回報應該是最基本需要做到的事情


### 2. 對於 bug 沒有危機意識
> 不知道事情的嚴重性？business sense ?

我覺得可以這樣改善

* 初期可以試著讓每個人 輪流 deploy production

> 當你要 deploy production 的時候, 你一定會比較謹慎
>
> 會注意到 deploy 完之後, 有沒有什麼 bug 出現, 會慢慢的培養對 bug 的敏感度

### 3. 如何開始 devops

> 扯一下現在很紅的 devops, 我是覺得要當一個好的 RD, 其實也要當過一陣子的 operation
>
> 因為假如你有維運的經驗 其實你會知道寫程式時 哪些地方要特別注意 哪些地方要特別加 log, 以利之後查詢
>
> 這其實也是一種自己的 feature 自己維運的概念 (但這又牽扯到未來的 micro-service 概念, micro-service 的一個很重要的點應該是 Boundaries and Responsibility )

  我覺得可以這樣開始：

  * 如果在一團混亂中, 最重要的是要先訂立基本的規範, 讓大家遵守, 而不能只是靠某些人的自動自發
  > 一開始先有資深同仁專責, 負責 operation 上的監控, 建立起基本維運所需注意事項流程, bug 回報處理機制

  * 再輪班每週專人負責監控 處理 bug ([honeybadger](https://www.honeybadger.io/), 或其他 issue) (但前題是大家都需要看 [honeybadger](https://www.honeybadger.io/), 自己的 bug 要自己解)
  > 輪班負責後, 大家也會對於系統 bug 問題敏感度更高, 也會更加了解系統
  每週輪班維運人員必須要整理需要監控的地方, 異常處理回復的工具, 並且加入 sprint 的需求中, 如此也可慢慢養成 devops 的觀念
  >
  > 輪班是因為要先有人負責, 防止大家都沒人去處理, 至少有人會去意識到問題的嚴重性

### 4. 如何加快團隊步調
  我的想法是

  * 拉快 review 節奏 團隊的步調自然就會加快

  > 而 review 的重點其實不是結果, 而是有進度
  >
  > 這樣做的好處是: 同事會知道無法每天都是同樣的進度
  >
  > 而且 leader 也會更明確的知道無法完成的難處, 並且給予協助
  >
  > 如此應該只要持續個一個月 必定能改變團隊整個的做事步調 方式

### 5. 沒有 ownership

  > 模糊地帶的問題, 沒人管
  >
  > 常常有計畫了 卻沒去執行

我的想法是

  * 如果有這種問題 leader 可能必須自己先以身作則, 當個有 ownership 以及 leadership 的人 先做團隊的榜樣

  > 具備這種特質的人, 通常會自己去找方法, 資源來解決問題, 而且也通常會知道團隊到底有什麼問題 並且帶領團隊解決

  * 我覺得團隊的文化, 是取決於 leader 是什麼風格, 因為文化的形成是一個上行下校, 不斷累積的過程, 因此 leader 的以身作則是相當重要的


### 結語

  這只是和朋友聊天, 討論的一些感想

  * 一個好的環境是非常重要的 你可以學習到正確的態度與流程 尤其是對於新鮮人而言

  * 另外也覺得 人才非常重要, 但更重要的是, 誰來帶領這些人才

  > 如果有一個好的 leader 我相信上述的問題
  >
  > 即使發生 也會很快的解決 若不能及時解決
  >
  > 也會讓你感受到團隊是有往好的方向的發展
