## 5) Project trajectory, results and interpretation

1) Briefly summarize any changes
Skip this already tackle in introduction?

2) Results
- model performances
- interpretations
- meaning of results
- impact of our work

I EDA
II models performances
III Polls



### I) Exploratory Data Analysis on socio-economic predictors

Let's present our findings on the relationship between socio-economic predictors and elections.

**In this EDA, we have average socio-economic predictors over the year.** We will see in the next part that these predictors do not vary much over our observation time of eight years).**

The following database shows the statistics about racial data of districts that have not change during the last five elections (remained Democrat or remained Republican).

![im1](pictures/All_democrat_statistics_race.png)

![im2](pictures/All_republican_statistics_race.png)

The different statistics shown above seem to show some quite significant differences when it comes to the origins considered. For instance, the percentage of non-hispanic white Americans seems higher (higher mean and smaller variance). Visually, let's compare the distribution of different races between Democrat and Republican strongholds.

The next plot compare the distribution of races between Democrat and Republican strongholds:

![im3](pictures/Boxplots_Race_EDA.png)

A couple of elements might be worth noting:
- Caucasian: Republican districts have higher means with a distribution much narrower.
- African American: Republican districts' distribution of votes is on the bottom side.
- Asian: Democrat districts seem to have more Asian voters than Hispanic voters.

The next plot presents compare the distribution of income classes between Democrat and Republican strongholds

![im5](pictures/Boxplots_Income_EDA.png)

There is an interesting trend that appears in the previous plots. It seems that in the Democrat strongholds contain the lowest income population subgroup, as well as the highest income - even though those districts might not be the same (c.f. two last plots - highest income and below poverty level).

The next plots presents the distribution of classes of jobs among Democrat and Republican stronghold:

![im6](pictures/Bars_age.png)
![im7](pictures/Bars_occupation.png)

A noteworthy pattern is that in the Republican strongholds the average distribution of unemployed inhabitants seems higher than in Democrat stronghold. However, in the different plots presented about the income level, the democrats' districts were "more prone" to have people living below the poverty level. One of the interpetation might be that the poorest people might be only a extremely limited part of the unemployed population.

The matrix below show us the absolute values of the correlation coefficients between our predictors. We have to be careful not to misinterpret the socio-economic predictors as they are proportions in a district.

![im8](pictures/Correlation.png)

This matrix justifies that our predictors are correlated. Some correlation makes sense like the proportion of low salaries and of unemployment. Hence we could use a method to select features or to decrease the number of features like Principal Analysis Component.

### II) Model performances

#### A) Baseline model

![im1O](pictures/Results_Basemodel_WithElectionInfo.png)
![im11](pictures/Results_Basemodel_WithoutElectionInfo.png)

#### B) Temporal stability of socio-economic predictors

The variability of the socio-economic predictors over years does not affect much the global population in a district. The only predictors which changes significantly only concern a tiny proportion of the whole population.

To quantify this statement, let's study the variance of each of these predictors. All of these predictors represents proportions of the global population.

Let's calculate the variance of the relevant predictors in each district over the last 5 elections.

[im20](pictures/Hist_STD_per_district.png)

The standard deviation represents the order of magnitude of the percentage of the whole population affected by the changes of these predictors.

Almost all standard deviations are lower than 2%. It means that the variability of these predictors affect less than 2% of the whole population, hence they are neglictible. It makes sense with the fact, that during 8 years, the socio-economic factor of a population doesn't really change.

Therefore, we can use the average values of these predictors to understand if they can explain wether a district is a safe stronghold or rather a swing district.

The figure below shows how noisy our data is : political noise. We see how close Democrat and Republican elected districts are with our PCA which can not accurately create a descision function

[im21](pictures/noisiness_proximity_points.png)

[im30](pictures/less_noisiness_with_model.png)
