patent
======

patent information mining
#所看文献总结2014-09-06
##Patent introduction
这几天看了几篇文献，以**patent**作为关键字，在SCI-E数据库查询。涉及到**Patent**的研究是很多的，只是我在思考如何将我以前研究的内容利用上，使得有一定的连续性。所看文献总结如下:
###1. Patent Maintenance Recommendation with Patent Information Network Model
####Author：韩家伟
#####Publication：2011 11th IEEE International Conference on Data Mining
> 这篇论文主要研究的内容是关于如何判断patent价值，为是否对其进行维护（缴纳维护费用）提供决策支持。
1.1 维护决策量化指标
+ writing quality--评判写作价值主要是利用文本统计的方式，对专利中不同部分所使用的词汇进行统计，判断是否相似。这里所谓高质量的专利就是说内容基本一致，词汇使用相似即可。**这里的标准是否应该这么定呢？疑问！**
+ novelty of patent--首先利用文本挖掘技术提取出专利中所使用的技术信息，然后利用专利数据库的年代，对所用技术的新颖性进行判断。这个比较简单，容易实现。
+ 所使用技术的价值--同上。就是越新的技术，价值越大。
+ 所使用技术的范围--有根据技术大类对，专利中的技术涉及范围评估，当然所涉及的技术领域越广越好。
+ 经济价值--文中这个没有解决，将经济价值扔给企业自主评判。
1.2 Patent tool
+Google patent search
+micropatent
+Delphion
+patent classification system（USPC）
+international patent classification system（IPC）
1.3 实验数据属性
+publication year
+filed year
+kind
+inventor
+assign class
+ZPC code
+cited patent
1.4 write quality measurement
+novel words
+声明完备性（KL-divergence）
+技术趋势
+发明者信息（PCount、ECount、EPratio）
+专利代理人信息
1.5 patent prediction model
使用decision tree进行预测
1.6 模型复杂性分析（这个我发现韩的文章基本都有这个，以后借鉴一下）
+feature extraction O(n)
+profile feature O(mn)
+refinementO(I|E|)
