# TikTok AML一面

> AML stands for Applied Machine Learning

Q: Can we use Chinese?

A: 我们可以说中文😅

先自我介绍，主要说了下和Tan的工作。

然后面试官表示他是Deep Learning Compiler组的manager。跟我overlap不高，所以也没多说啥。还表示我申的是CA的岗位？连忙表示我人还在国内。他说他们在北京，上海，杭州都有组，那我就prefer China了。

然后又问了问在Microsoft和RisingWave Labs干了啥。表示都和MLSys没啥关系。

然后问了问你是怎么优化transition的，糊了一通，看起来他不太了解这块也没有深究。

## LCA

> 🥰昨晚刚看过。
>
> 🤡可惜没写code。
>
> 😇他也没让我写code。

感觉coding考察的非常随意。我先说了最straightforward的。两个节点先跳到同一深度再往上一起跳。

深度怎么办？DFS

咋往上跳。好问题，如果有指向父节点的指针就好办了。那就有这个指针吧。

时空复杂度。

DFS是O(n)... 你有父指针还要DFS吗？有道理，直接遍历到root就行了。那就O(h)

现在不让你用深度了，怎么做？

思索了一下，这个不就是俩链表么，我可以先跳到root再跳到对方的node再往上跳，重合的时候肯定是LCA。他表示这个做法非常有趣，但我觉得不work（😅）

又提示了一下你可以记录从root到它的路径。有道理，那我就拿个线性表记然后比一下。

线性表好慢好慢。那就set。对了嘛，那你分析下时间复杂度。O(n log n)。你log咋来的。红黑树嘛。哦应该用哈希表。那就O(n)。空间呢？这个跟hash function有关吧。

> 全程聊天，甚至pseudo-code都没写

## about AML

这个组是分布式的，中国，坡，美西（湾区，Seattle），纽约啥的都有。

大概一共150个人。

有做training的，inference，compiler的，还有做model的，让准确率更高一点。

你大概率会顺着之前tan的工作继续做。

我表示因为搞过k8s，最近也在研究k8s和GPU的一些应用，所以想做点GPU和cloud相关的东西。

下一个面试官估计是做training的，到时候你可以和他详细聊聊你的project。cool~
