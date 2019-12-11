# Introduction
![2018 final results](pictures/all_results.png)

## Background
The 2018 midterm elections were hold on November, 6th, 2018. 435 seats were contested. Each seat represents a district which is a part of a single State and includes around 700,000 people. The boundaries of a district is refined every ten years to ensure equal number of people in every districts.

President Donald Trump was the incumbent Republican President. The Republican lost the elections (199 seat for the Republicans and 235 for the Democrats, one Representative identified himself as independant). A loss at such extent for the Party holding the Presidency during the midterms has not been seen since 1990 [6].

The midterm elections are crucial for the government. The outcomes will dictate the second part of the incumbent President term. If the latter won a majority in both houses of the Congress, it ensures him free hand to conduct its politics.

Predicting the election is essential for campaign and political advisors. Having some insights about the most impactful predictors can help guiding the candidates into finding the right strategy to gain the support of more electors. Predicting and studying past elections can provide valuable information. But more importantly, understanding what are the factors that govern the vote goes one step further in the entire approach.

## Why is predicting a challenge ?
Predicting the elections' results is strongly related to understanding human behavior: why would one find a candidate or party appealing?  Even if we have access to very detailed socio-economic variables or precise polls, there are abstract or latent variables that will the trend. Elements such as _popularity_, _mood_, or _influence of media_ are difficult to quantify, to detect or even define. Hence, we can cast doubt on predictions due to unknown parameters which can significantly influence the outcome.
![Presenting the noise within the data](noisiness_proximity_points.png)

### Problematic
What are the economic, social or demographic factors that are the most influential to predict the popular vote? Are those actually accurate predictors?

In our preliminary work, we first collected information accross districts for instance about poverty, unemployment, or social origin during the last five elections. We notice that these factors have not been varying much through this last decade. Hence they are not sufficient to explain why some districts have different election results through years because these factors are almost constant. However they can help us to single out if a district is a Republican or a Democrat stronghold or rather a swing district. Finally, we also extended our study in time. Polls are a great indicator of the vote intentions at different time before the elections. Having the evolution of vote intentions before the elections can help us identify which political or social events can influence electors.

### Description of data

The following data was gathered, for visualization, exploration and model fitting. 

1. **House of States Results**

Harvard’s Dataverse and FEC report [2,3]  were combined in order to obtain the different percentages of votes assigned to each candidate for a given district. To simplify those results, the team made the assumption that the results of a vote could be limited to classes: ‘main republican candidate’, ‘main democrat candidate’ and ‘other’. This approximation is far from being crude in practice and is experimentally verified. These results are considered as the labels.

2. **Origins dataset**

These date were extracted from observations of the US Census Bureau (Population division) [11]. It contains the total numbers of male and female in different ethnical group at the counties levels from April 1, 2010 to July 1, 2017. We sum these numbers, to obtain the proportions of these groups per districts.

3.**Poverty and unemployment**
?? => Théo

4.**Education**

For the baseline of the milestone 3, we used data on education. However these data were at the States level, it was too inaccurate to attribute to counties or districts these States values. 

5.**Polls** 

Polls data are scraped from an article from the Huffington Post [10] that list polls from the 2018 midterm elections for the House of States. All these polls are made at a national level, and can help us to predict the popular vote. The information available include the percentage of vote for the Democrats, the Republican and other parties, the percentage of undecided voters, the starting and ending date and the source. The polls where conducted from January 2017 to November 2018 (a few days before election day).
