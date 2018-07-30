# COMPUTER AGE STATISTICAL INFERENCE

## Algorithms and Inference

Statistics is the science of learning from experience, particularly experience that arrives a little bit at a time: the successes and failures of a new experimental drug, the uncertain measurements of an asteroid's path to-ward Earth. It may seem surprising that any one theory can cover such an amorphous target as "learning from experience." In fact, there are *two* main statistical theories. Bayesianism and frequentism, whose connections and disagreements animate many of the succeeding chapters.

统计学是一个从经验中学习的学科，尤其是*每次得到一点点的经验*：一种新型试验药的成功与失败，小行星驶向地球路径的不确定性测量。任何一个理论都能*适用*这样一个模糊的目标：“从经验中学习”，这似乎令人惊讶。事实上，有两种主要的统计理论。贝叶斯主义和频率派，它们的联系和分歧推动了许多后续章节。

*ps: at a time 指依次、逐次、每次；at one time 一度、从前*

First, however, we want to discuss a less philosophical, more operational division of labor that applies to both theories: between the *algorithmic* and *inferential* aspects of statistical method, averaging. Suppose we have observed numbers $ x _ { 1 } , x _ { 2 } , \dots . . . x _ { n } $ applying to some phenomenon of interest, perhaps the automobile accident rates in the n = 50 states. The *mean*
$$
\overline { x } = \sum _ { i = 1 } ^ { n } x _ { i } / n
$$
Summarizse the result in a single number.

然而，首先，我们要讨论适用于两种理论的较少哲学，更具操作性的分工：统计方法的算法和推断方面之间的平均。假设我们观察到某些我们感兴趣的数： $ x _ { 1 } , x _ { 2 } , \dots . . . x _ { n } $ ，就当是 50 个州汽车事故率，它们的均值是：
$$
\overline { x } = \sum _ { i = 1 } ^ { n } x _ { i } / n
$$
将结果汇总到一个数值中。

How accurate is that number? The textbook answer is given in terms of the *standard error*,
$$
\hat { s e } = \left[ \sum _ { i = 1 } ^ { n } \left( x _ { i } - \overline { x } \right) ^ { 2 } / ( n ( n - 1 ) ) \right] ^ { 1 / 2 }
$$

Here *averaging(1)* is the algorithm, while the standard error provides an inference of algorithm's accuracy . It is a crucial, aspect of the statistical theory that same data that supplied an estimate can also assess its accuracy.[^1]

这里平均（1）是算法，而标准误差提供算法精度的推断。 统计理论的一个重要方面是，用于估计的数据也可以评估其准确性。

Of course, $\hat{se}$ (3) is itself an algorithm, which could be (and is) subject to further inferential analysis concerning *its* accuracy. The point is that the algorithm come first and the inference follows at the second level of statistical consideration. In practice this means that algorithm invention is a more free-wheeling and adventurous enterprise, with inference playing catch-up as it strives to assess the accuracy, good or bad, of some hot new algorithmic methodology.

当然，$\hat{se}$ 本身就是一种算法，它可以(而且是)对其准确性进行进一步的推论分析。 关键是算法首先出现，*推断遵循统计考虑的第二个层次*。 在实践中，这意味着算法发明是一个更加自由和冒险的事业，当它努力评估一些热门的新算法方法的准确性，无论是好还是坏，推断都在追赶。

If the inference/algorithm race is a tortoise-and-hare affair, then modern electronic computation has bred a bionic hare. There are two effects at work here: computer-based technology allows scientists to collect enormous data sets, orders of magnitude larger than those that classic statistical theory was designed to deal with; huge data demands new methodology, and the demand is being met by a burst of innovative computer-based statistical algorithms. When one reads of “big data” in the news, it is usually these algorithms playing the starring roles.

如果推理/算法竞赛是一场龟兔赛跑，那么现代电子计算已经培育出了一只仿生兔子。这里有两个效应: 基于计算机的技术允许科学家收集大量的数据集，这些数据集的数量级要比经典统计学理论所要处理的数据大得多;巨大的数据需要新的方法，而需求正被大量创新的基于计算机的统计算法所满足。当人们在新闻中读到“大数据”时，通常是这些算法扮演主角。

Our book’s title, Computer Age Statistical Inference, emphasizes the tortoise’s side of the story. The past few decades have been a golden age of statistical methodology. It hasn’t been, quite, a golden age for statistical inference, but it has not been a dark age either. The efflorescence of ambitious new algorithms has forced an evolution (though not a revolution) in inference, the theories by which statisticians choose among competing methods. The book traces the interplay between methodology and inference as it has developed since the 1950s, the beginning of our discipline’s computer age. As a preview, we end this chapter with two examples illustrating the transition from classic to computer-age practice.

我们这本书的标题，计算机时代的统计推断，强调了乌龟的一面。过去几十年是统计方法的黄金时代。这并不是统计推断的黄金时代，但也不是黑暗时代。雄心勃勃的新算法的繁荣期迫使推断(尽管不是革命)发生了变化。推断是统计学家在相互竞争的方法中选择的理论。这本书追溯了方法论和推理之间的相互作用，从20世纪50年代开始，也就是我们学科计算机时代的开始，这本书就开始发展。作为一个预览，我们结束这一章的两个例子说明从经典到计算机时代的实践的转变。	

[^1]: "Inference" concerns more than accuracy: speaking broardly, algorithms say what the statistician does while inference says why he or she does it. - “推断”不仅仅关注准确性：从广义上讲，算法说明统计学家所做的事情，而推理则说明为什么他或她这样做。

### A Regression Example

Figure 1.1 concerns a study of kidney function. Data points $(x_i , y_i$ have been observed for n = 157 healthy volunteers, with $x_i$ the *i*th volunteer’s age in years, and $y_i$ acomposite measure “tot” of overall function.Kidney function generally declines with age, as evident in the downward scatter of the points. The rate of decline is an important question in kidney transplantation: in the past, potential donors past age 60 were prohibited, though, given a shortage of donors, this is no longer enforced.

The solid line in Figure 1.1 is a linear regression
$$
y = \hat { \beta } _ { 0 } + \hat { \beta } _ { 1 } x
$$
