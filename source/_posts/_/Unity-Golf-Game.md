---
title: Unity Golf Game
date: 2022-11-25 14:02:16
tags:
categories:
---

## 來做糞Game - 高爾夫球遊戲 - 新手版

[重構版]()

######

[乾淨版]()

### 緣起

看到糞Game廣告，覺得自己也要做一個糞Game

### 美術風格

Simple 3D，因為我沒有美術實力，又是免費仔，所以本文的美術資源都是台式極簡手拉風

### 操作

在球上拖曳、放開，將球彈走，在球以外的地方拖曳可以改變視角

### 使用工具

+ Unity 3D
  + 3D World Building
  + Cinemachine

### 預計釋出平台

+ Windows

### 實作順序

1. 球體與擊球功能
2. 終點判定
3. 計分規則
4. 攝影機控制
5. 特效與其他要素完善
6. 開始與結束畫面
7. Build

### 開發步驟

開啟Unity，建立3D專案，引入Package

> 建立Unity專案 可以參閱 [此文章]()，Package介紹看[這裡]()，哈。

### 球體

右鍵建立一顆球體(Sphere)，跟一塊地(Plane)，對著球體加入一個Script後，我們就來定義核心玩法：「拖曳」吧。
拖曳的操作流程是：點擊（按住）畫面上某個位置，移動到另一個位置後放開。
>隱憂：如何區分點擊與拖曳?

1. 先做判斷：是否點擊在球體上？如果是，就進入準備擊球的狀態。
2. 點擊在球上，會紀錄擊球點，擊球點是力作用在球體上的位置
3. 鼠標拖曳
   1. 拖曳長度：力的大小
   2. 拖曳後的相對位置：力的方向

> 這個GameObject會需要：Collider, Rigidbody，請記得掛上才會work
>
有了以上資訊，我們就可以依照去填入對球產生的力的操作

<details>
<summary>關於 RidgidBody 你可能想知道的事</summary>

+ [RigidBody實驗+Gif動圖解說]()
+ [官方文件](https://docs.unity3d.com/ScriptReference/Rigidbody.AddForceAtPosition.html)

</details>

``` C#
class myclass
{
  string a = "123";
  void code() 
  {
  //TODO
  }
}
```

## 終點判定

擺放一個物件，圓的方的都可以，然後掛上一個Script

```C#

```

## 攝影機控制

從各種角度擊球

## 計分規則

這時候你會發現，阿分數要去哪裡存，沒錯，我們就再加入一個Script，單純存放玩家分數。

```C#
```

連接程式

## 特效與其他要素完善

顏色，更多的球，快還要更快，多還要更多，打擊感，關卡設計

## 開始與結束畫面

這才是完整的遊戲

## Build



