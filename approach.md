# Approach, models and assumption.


## Modelling assumptions
- Let's recall that the datatset, after the full cleaning process consits of (socio-eonomic and demographic) SCD indicators for each pair (district, year), with the years ranging from 2010 to 2018 (predictors). The label is a 3 class vectors representing whether the elected candidate is "republican", "democrat" or "other".
- In the first place we decide to neglect the "other" candidate which is factually an edge case (38 cases over the entire dataset).
- Furthermore, e formulate the hypothesis that providing a model with the history of elected candidates might improve a model predictive power (indeed, some districts are historically republican and not prone to any change, and reversely). Therefore, we explore two scenarios: one including an indicator

Add history fo past--> Compare models with/without
- Boosintg, ...., ---> SOme= accurate]

## Look for understanding 
- Predcition is important but further 
- Extremeley close points. Non-identifibality
- 'Political noise' - variance over time negligeable -> Picture Noise. + HIsti+STD per district. 
Less noisiness. 

- Urges us to put into practice those
- Dimensionality reduction
- Logitsi regression woth Lasso--> *Bootsrap, smot to takcle the pb of feat. importance. 


### Temporal stability of socio-economic predictors

The variability of the socio-economic predictors over years does not affect much the global population in a district. The only predictors which changes significantly only concern a tiny proportion of the whole population.

To quantify this statement, let's study the variance of each of these predictors. All of these predictors represents proportions of the global population.

Let's calculate the variance of the relevant predictors in each district over the last 5 elections.

![im20](pictures/Hist_STD_per_district.png)

The standard deviation represents the order of magnitude of the percentage of the whole population affected by the changes of these predictors.

Almost all standard deviations are lower than 2%. It means that the variability of these predictors affect less than 2% of the whole population, hence they are neglictible. It makes sense with the fact, that during 8 years, the socio-economic factor of a population doesn't really change.

Therefore, we can use the average values of these predictors to understand if they can explain wether a district is a safe stronghold or rather a swing district.

The figure below shows how noisy our data is : political noise. We see how close Democrat and Republican elected districts are with our PCA which can not accurately create a descision function

![im21](pictures/noisiness_proximity_points.png)

![im30](pictures/less_noisiness_with_model.png)




## 1 -  


## 2- 

Our baseline model is a logistic regression that predicts the results of each district. This model takes in input some social-economic predictors with general political information. We have trained this model in the results of the House of States elections from 2010 to 2016 and we tested this model on the 2018 elections. 

2) description of our implementations beyond baseline with design choices

    a) Part Théo + Will
    



{% include lib/mathjax.html %}
