# 第八章筆記_memory Management_記憶體管理
###### tags: `作業系統`
# Contents
[TOC]

---
## **a. Binding**
- **address binding (位址定位):**
  決定使用者要從哪個處理程序開始執行位址。
  (簡單來講:從記憶體的哪個地方開始執行)
  
  ***<Binding 時期>***
  1. compiling time
  2. loading time
  3. execution time
  
  <圖一>![](https://i.imgur.com/eXayg4B.png)
  
 ### 1.  Compile time
  - binding 決定是compile time後，接續程式執行的起始位址會被固定。
  - 如果要start location changes，只能recompile
  
  <圖二>![](https://i.imgur.com/gWctraD.png)
  
 ### 2.  Loading time
  - 會由linking loader 決定(參考圖一) 
  - linking loader: linking、allocation、loading、relocation
  - 如果要start location changes，reload the code就好，不用重新來過
  
  <圖三>![](https://i.imgur.com/qTMLF2X.png)

 ### 3.  Excution time
  - 由OS動態決定
  - 在excution time中，可以任意變更起始位址
  - 又稱dynamic binding 
  - 
  <圖四>![](https://i.imgur.com/945l6oi.png)
  
 ----- 
## **b. logical address v.s. phsical address**
### logical address
- 邏輯位址是虛擬的(virtual address)
- 會在CPU裡運作
	
---
## **c. dynamic loading**

---
## ** 動態記憶體配置**
- first fit->
最先適用：記憶體分配足夠大就使用，優點是簡單、分配速度快速，記憶體使用率也不算太差。
- best fit->
最佳適用：記憶體分配會使用與需求最接近的區塊，這樣使用分配後，所剩餘下來的各可分配記憶體區塊會最小，在記憶體的空間使用率較佳，缺點是所剩餘下來的區塊會比較零碎，而不足讓其他記憶體需求使用。
- worst fit->
最不適用：記憶體分配會優先使用最大的分區塊，這樣所剩餘下來的區塊會比較大，也比較有機會提供其他空間需求使用，缺點是記憶體空間使用率較差。

---
## **swapping**
---
## **dynamic storage allocation**

---
## **external fragmentation(外部碎裂) v.s. internal fragmentation(內部碎裂)**
### 1. external (外部碎裂)
- 所有free block的大小總和 >= process要求的大小，但free block不連續，不足以配置一個空間給process

### 2. internal (內部碎裂)
- 裡頭的某段free block大小 > process要求的大小，但沒有剛好一樣大，所以不給配置
- 
  
https://hackmd.io/@Chang-Chia-Chi/OS-CH8
  

