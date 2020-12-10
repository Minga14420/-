# 資安作業
在於listing_5_1.py中，會先抓取指定路徑上所有的檔案，並使用pecheck的副程式去確定檔案是不是PE檔，不是就丟掉。

在於threshold 0.8 與 0.3的差別是"兩者相似度的標準"。
在比較兩個malware的相似度時是以這次的作業來講，是使用jaccard分析作為去進行相似度判斷。
jaccard是藉由用要分析的兩者的交集除以兩者的聯集(交集/聯集)去判斷兩者的相似度，所以當得到的數字越高其相似度越高，反之。

所以如果threshold設為0.8，就表示使用jaccard算出的數字要大於等於0.8以上兩者就會進行連線，如下圖
![](https://i.imgur.com/P2cmFvG.png)

如果threshold設為0.3，就表示使用jaccard算出的數字要大於等於0.3以上兩者就會進行連線，如下圖
![](https://i.imgur.com/P24PSRW.png)

由上面兩圖來看就能明顯知道threshold 0.8 與 0.3的差別了。由於0.3的標準較低，所以在於各種不同的malware比較中，
