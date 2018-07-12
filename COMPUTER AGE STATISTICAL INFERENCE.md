# COMPUTER AGE STATISTICAL INFERENCE

## Algorithms and Inference

Statistics is the science of learning from experience, particularly experience that arrives a little bit at a time: the successes and failures of a new experimental drug, the uncertain measurements of an asteroid's path to-ward Earth. It may seem surprising that any one theory can cover such an amorphous target as "learning from experience." In fact, there are *two* main statistical theories. Bayesianism and frequentism, whose connections and disagreements animate many of the succeeding chapters.

统计学是一个从经验中学习的学科，尤其是*每次累计一点点的经验*：一种新型试验药的成功与失败，小行星驶向地球路径的不确定性测量。任何一个理论都能*适用*这样一个混乱的目标：“从经验中学习”，这似乎令人惊讶。事实上，有两种主要的统计理论。贝叶斯主义和频率派，其联系和分歧推动了许多后续章节。

First, however, we want to discuss a less philosophical, more operational division of labor that applies to both theories: between the *algorithmic* and *inferential* aspects of statistical method, averaging. Suppose we have observed numbers $ x _ { 1 } , x _ { 2 } , \dots . . . x _ { n } $ applying to some phenomenon of interest, perhaps the automobile accident rates in the n = 50 states. The *mean*
$$
\overline { x } = \sum _ { i = 1 } ^ { n } x _ { i } / n
$$
Summarizse the result in a single number.

然而，首先，我们想讨论一个不那么哲学的，更能操作的工作，它适用于两种理论：在算法和统计方法的推论方面，平均值。假设我们观察到某些我们感兴趣的数： $ x _ { 1 } , x _ { 2 } , \dots . . . x _ { n } $ ，就当时 50 个州汽车事故率，它们的均值是：
$$
\overline { x } = \sum _ { i = 1 } ^ { n } x _ { i } / n
$$
将结果汇总到一个数据中。

How accurate is that number? The textbook answer is given in terms of the *standard error*,
$$
\hat { s e } = \left[ \sum _ { i = 1 } ^ { n } \left( x _ { i } - \overline { x } \right) ^ { 2 } / ( n ( n - 1 ) ) \right] ^ { 1 / 2 }
$$
