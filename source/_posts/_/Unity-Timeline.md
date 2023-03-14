---
title: Unity Timeline
date: 2023-01-03 15:02:06
tags:
categories:
---

## Timeline

不同於Animator，Timeline更傾向於一段無玩家操作的動畫表現，因此Animator與Timeline可以並存

### Control Tack

可以撥放別的Timeline

### Activation

Activation 可以設定物件的Active狀態，並可以設定在Timeline 結束後，該保持何種狀態(有Active, Inactive, 反轉, 延續 四種)

### AudioClip

AudioClip 可以同步撥放與暫停音效

### TimeClip(custom)

TimeClip 可以撥放C#程式
在這個例子當中讓音效可以持續撥放而不被中斷

### Marker

Marker 可以在指定時間設上一個標籤，讓Signal使用

### Signal

Signal 可以跳轉至指定Marker，並在觸發時可以呼叫別的GameObject的程式Reciever(Interface)

### Animation Track

Animation Track 可以撥放與錄製 Animation，功能類似Animator

### Mixer

混合器，把不同的clip按照權重混合起來，例如撥放音效的track的mixer就可以做出漸弱漸強的轉換播放

### Cinemachine.Timeline

可以配合Cinemachine 做運鏡

>小習慣：把Timeline的物件做父子階層，可以更直觀的了解關聯關係

### Timeline 主要元素的關係

Timeline可以有很多Track，一條 Track 有很多 Clip，跟一個Mixer來整合

### Custom 自定義

即使Timeline很好用，也很有彈性，但也還是有需要自定義的部分。
寫出一個自製的Timeline功能需要四個程式
Mixer,playableBehaviour,clip,trackAsset
