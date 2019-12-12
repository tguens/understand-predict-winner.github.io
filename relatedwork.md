# Related work

Several experiments aiming predict the elections' outcomes have been conducted. For instance, in [[7]](https://ieeexplore.ieee.org/document/6113109), the author analyzes methods of prediction using sentiment analysis from social network data (notaby tweets, and google search results). They reached the conclusion that these methods are **not sufficient to predict elections**. 

The article [[1]](https://www.washingtonpost.com/politics/democrats-eye-house-takeover-to-challengetrump-as-gop-tries-to-hang-on/2018/11/06/2c4ff3a0-e200-11e8-8f5fa55347f48762_story.html) from *The Washington Post* presents the **electoral vote within different subgroups**: _age, sex, race, education sub-categories or even and among rural or city environments_. The conclusion reached, id est - within categories, the vote is significantly different - strengthened our prior belief that **understanding the most influential features** is key to our problem. It also urged us to collect more **socio-economic data**.

The research conducted in [[8]](https://github.com/tguens/understand-predict-winner.github.io/blob/master/references.md) explores the reasons why the **president's party suffers from an electoral decline** when come the midterms elections. In particular, they are looking for explanations conciliable and in accordance with historical records. The conclusion reached is that no matter what might happen on the political stand, the president's party will lose house representatives. 

In [[9]](https://github.com/tguens/understand-predict-winner.github.io/blob/master/references.md), the authors take a Bayesian approach to predict the United States Presidential elections. A relative simple model is proposed: polls (at a state level) are incorporated and the model assumes a normally distributed distribution around the results of the elections. With a prior belief and polls data, the authors end up estimating the posterior distribution of the results. They also claim that their method is effective to handle swing states. 


However, those models only consider data at a state or country level and oftentimes focuses on American presidential elections.
Our work **unifies** some aspects of the aforementioned research and analysis. Precisely:
* We **collect, gather, and create an entire dataset** at the district level, with socio-economic, demographic and ethnic variables.
* We present a set of assumptions such as averaging over the years in order to **present accurate predictive models**.
* We present an analysis of the features that appear to be the most 'important' for a voter to vote for a republican or a democrat candidate.
* We further include a **bayesian hidden model** to estimate the political volatilty and show that it is relatively accurate when it comes to predicting the popular vote. 


[Next page: Approach](https://tguens.github.io/understand-predict-winner.github.io/approach.html)

[Previous page: Introduction ](https://tguens.github.io/understand-predict-winner.github.io/intro.html)

[Back to main](https://tguens.github.io/understand-predict-winner.github.io/)
