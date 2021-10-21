# 统计建模之道和术：追根溯源

 
## 摘要

对任何想解决现实世界问题的统计学者来说，Leo Breiman的文章《统计建模：两种文化》都是宝贵的财富。而我认为，相比数据模型、算法模型的分类，以原则、技术来划分统计建模更为本质。仅仅关注统计教育和研究中的技术可能是危险的。我赞同Breiman的呼吁，统计研究应该追根溯源。

关键词：Leo Breiman；因果建模；统计哲学

## 我的观点是如何变化的

Leo Breiman的《统计建模：两种文化》在出版20年之后仍然是一篇非常鼓舞人心的文章。我最欣赏的是，Breiman详细而坦率地叙述了在职业生涯中，他对统计的看法是如何改变的。对于像我这样前开始职业生涯的年轻统计学者来说，这是宝贵的财富。

我读过Breiman的文章三次。第一次在我博士早期2013年，我看到Jerome Friedman教授在一个研讨会上对Breiman深情致敬。他回忆了在20世纪80年代，他和Breiman在统计领域中推进机器学习（或“算法建模”文化，参照Breiman文章中的术语）中的种种困难。他还感叹到，如果Breiman没有在2005年去世，之后就能看到机器学习的爆炸式发展，将会是多么的高兴！然而，我并没有从第一次读Breiman的文章中收获多少。Breiman文章中的大部分想法对我来说都很自然；因为在斯坦福大学统计系的课堂和研讨会中，这些内容我都刚刚学过。斯坦福大学统计系深受Breiman思想的影响。

2016年完成博士学位后，我又读了Breiman的文章。那时，我了解了因果推断的一些知识，而且被这个领域中瑰丽、奇特的想法迷住了。当时，因果推断还是一个利基研究领域；至少我周围很少有人对它感兴趣。我拼命地寻找因果推断和“主流” 统计（不管我如何认为）之间的联系，但我找不到很多。除了一个巧合，Friedman解释黑盒算法的部分依赖图（partial dependence plot）与因果识别的混杂因素调整（或后门调整）公式完全相同。如果参照Breiman文章的术语，把这个要小得多的领域称之为“因果建模” 文化；那么我估计，在2016年“因果建模”人数将与Breiman在2001年对“算法建模”人数的估计相当：“2%的是统计学者，大部分在其他领域”。由于我当时已经看过很多关于“数据建模”的糟糕例子，这次我可以更好地欣赏Breiman的观点。

当然，最近一次读是在我准备为《观察性研究》写这篇评论的时候。这次，我学到了更多关于因果推断的知识，而且在剑桥大学刚刚完成了本科生的统计建模和研究生的因果推断的课程教学。这些经历帮助我更批判性地看待Breiman的观点。尽管我依然同意文章中的许多观点（特别是Breiman呼吁统计学“追根溯源”），但我也开始对另外一些观点感到怀疑。下面我将阐述一些我赞同或不赞同Breiman的地方。

## 技术与原则

Breiman的“数据建模”和“算法建模”之二分法是一个强大的分类方法，仍然广泛存在于今天的教科书和文献中。虽然人们的观点几乎总是不断变化的，但我可以理解为什么Breiman决定在两个极端之间作出鲜明的对比。然而，随着机器学习的重要性在统计学中越来越普及，将统计建模分为“数据模型”与“算法模型”不再有帮助。我认为这两种文化之间的界限如果现在还有，也是非常模糊的。

我认为，一个更基本的二分法，是在统计建模的原则和技术之间。中国人把前者称为道 （“路线”、“原则”或“思想”），后者称为术（“技术”、“技巧”或“方法”）。 很难准确地描述哲学上的差异，但以下大致是我的想法：

1. 技术或术：在这种观念下的分析始于一些由其他人准备好的数据集。我们的目标是尽可能好地分析数据集，但具体的任务通常取决于分析方法的复杂程度。可以像一个简单的线性回归一样简单，也像一个有十亿个参数的神经网络一样复杂。

2. 原则或道：这种观念的分析始于科学、工程或商业问题。其目标是了解问题背后的机理，并利用洞察结论来更好地决策。这可能是估计某种干预的因果效应或理解数据集的局限性。

我来尝试举一个更具体的例子。我定期在我们实验室组织的“统计诊所”服务，那里为剑桥大学的成员提供免费的咨询。在诊所里，我遇到了很多需要统计方法帮助的人。我们的对话通常从客户问我开始：“我如何将这个模型用到我的数据集上？”我的回答是：“你为什么要套用这个模型？”然后我通常会要求客户描述他们的科学问题。令人惊讶的是，他们经常告诉我，他们的合作者或主管只是给了他们数据集，并希望他们使用这个模型。偶尔，我能更好地理解他们的问题，并最终向他们提出一个不同的模型。但不幸的是，我的客户很少对更好的模型感兴趣。通常是因为没有软件可以立即使用，因为我建议的模型是针对他们的问题量身定制的。这得有多讽刺啊！

我怀疑，大多数参与现实世界问题的统计学者都有类似的经历。似乎大多数数据分析人士都更强调技术，而不是原则。但是，只有以良好的原则为指导并应用于正确的问题时，技术才是好的。从根本上说，技术驱动建模和原则驱动建模的区别在于，前者文化将统计建模视为为数据选择最佳模型，而后者文化将统计建模视为做出更好决策的手段。这些目标并不总是相互冲突的（例如，如果一个更好的决定意味着对下一个观察结果有更好的预测）。然而，大多数情况下，这两种心态会导致非常不同的模型和分析。 

## 统计建模的循环视图

技术驱动的文化可能相当危险，尤其是对高风险问题。一个很好的例子是去年对新冠疫情大流行的早期分析，我写了几篇文章和评论。 一个特别著名的例子是，一些非常具影响力的研究甚至没有正确估计指数增长曲线的速率。一个简单的泊松对数线性回归可以很好地达到这一目的，但传染病建模由部分动态模型（compartmental dynamic models）主导。这种模型对做出预测很有用，但当分析师只有早期的爆发数据时，通常会被过度识别。为了解决这个问题，大多数分析师只是对一些模型参数进行了非常粗略的估计，而忽略了这些估计中的不确定性。这通常会导致糟糕的拟合、看似很小的置信区间和荒谬的结果。一个臭名昭著的例子是牛津大学传染病进化生态学小组的一项研究。通过设置重疾患者人口的比例在一个非常小的值0.1% （数据从中国和意大利已经表明感染死亡率远高于0.1%），论文表明，可能有一半的英国人口已经在2020年3月19日被感染了。事后看来，这个结论显然很荒谬，但这项研究立即被媒体拱了新闻头条。它在关键时刻造成了不必要的混乱，并被被动的“群体免疫”方法（通过病毒感染而不是疫苗获得的免疫）的支持者用来批评政府的公共卫生干预措施。

顺便说一句，最后一项研究可能在一定程度上是由先入之见和政治驱动的，作者选择性公布他们极其初步的结果，而之后为臭名昭著的大巴林顿宣言（Great Barrington Declaration）辩护。每个统计学者都知道有选择地报告和分析数据是多么的容易和危险，特别是当一个人已经有了一个预想的结论时。我希望这永远不会成为统计建模中的一种“文化”。

当我试图理解统计建模的技术与原则的二分法时，我发现下面来自Box（1957）特别尖锐的评论：

    科学研究通常是一个迭代的过程。“猜想-设计-实验-分析”的循环周而复始。在考虑统计问题时，在脑子里牢牢记住整个实验过程全景图是有很帮助的。虽然这个循环在研究过程中重复了很多次，但实验环境和适合设计和分析的技术往往会随着研究的进行而发生变化。

所以，原则或道是很重要的，因为它们为我们提供了一个统计研究的整体观点，并指导技术的使用。同时，这些技术或术也同样重要，因为它们促进我们实践和改进统计建模的原则或道。

## 追本溯源

从表面上看，我似乎是在批评Breiman对“算法建模”文化的推广。毕竟，决策树和神经网络只是比线性回归、逻辑回归和Cox模型更好的预测分析技术。然而，我认为原则与技术的二分法通常在不同的时间采取不同的形式。2001年，统计学上最显著的划分是在“数据建模”文化和“算法建模”文化之间，但过去20年里情况发生了巨大变化。对于我这一代的统计学者来说，来自机器学习的想法可能比来自经典统计学的想法更有影响力。我的一些同行已经把线性和逻辑回归等“数据模型”当成过时的技术，并把神经网络作为现实世界问题的默认选择。

但Breiman的文章不仅仅是“数据模型”与“算法模型”或经典统计数据与机器学习。在最后的讲话中，他明确表示，他“并不反对数据模型本身……但重点需要关注问题和数据。”在最后一段，他总结道：“统计学的根源，就像科学一样，在于与数据合作，用数据验证理论。我希望我们的领域在本世纪能回到它的根源。”我完全同意这些观点。 

目前，机器学习领域正在进行在一场向何处去的争论，少数研究人员呼吁进行一场 “因果革命”。这在统计学上可能争议不那么大。我遇到的大多数统计学者都认识到因果推断的重要性，并真的有兴趣了解更多。但这并不总是那么容易，因为因果关系的概念在统计学教育中很大程度上是缺失的。

一个更大、更基本的问题是，大多数博士统计学者（包括我）都接受了开发新技术的训练，大多数数据分析师也接受了应用这些技术的训练。这不仅仅是一个当代的问题；Tukey（1961）在60年前就已经注意到了：

    涉及统计和定量方法的研究问题……这是一个存在于高等教育和文化人类学范畴下的科学家中的问题：为什么仅有如此之少的人能学会很好地分析数据？

Tukey建议，每个社会和行为科学的博士都应该经历Box的统计研究周期，最明智的顺序是 “分析-猜想-设计-实验-分析”。我同意这一点，但也想说，顶级统计期刊上的大多数论文并不是这样撰写或评估的。

最后，我想以中国经典《道德经》的首句结束。“道可道，非常道”（可以说清楚的道，不是恒久之道），我认为这句话同样适用于统计建模，从来没有绝对正确的统计实践或教学。但这也正是为什么统计建模如此迷人的原因。