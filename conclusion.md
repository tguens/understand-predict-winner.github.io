# Conclusion


What are the economic, social or demographic factors that are the most influential to predict the popular vote? Are those actually accurate predictors?

To do so, our group first built a base-line model that used past election results and yearly features. This model performed really well but lacked in explainability because of the low variance from year to year in our features per district and because of political noise.


To tackle those 2 challenges, we had two parallel approaches, aggregate our data at a district level to limit the noisiness of our data and concentrate on the explainability of the prediction to understand the consequences of events on popular opinion.


We can now conclude that it is **the combination of political events, policies and economic, social or demographic factors that guide the decision to vote for the Democrat or Republican party**. 

- Main factors such as **the proportion of African-American, Asian origin,Transportation jobs and Business owners** are highly linked to 'swing districts'. They seem to cause variability in the elections outcomme year in year out.

- Notable, the rejection of immigration reforms and the nuclearization pact with North Korea were highly correlated with shifts of popular opinion in 2018.




Future work: 
- As mention in the section concerning polls it would be interesting to add granularity to this model. Indeed, we only focus on the popular vote but we could also replicate these smoothing and predictions at the district level which would enable us to make predictions in term  of number of seats.
- We could also try to collect data about the candidates. The advantages of these data compare with social-economic predictors is that they will actually vary between elections. Hence, we could try to describe the succesful Republican or Democrat candidates.


[Next page:](https://tguens.github.io/understand-predict-winner.github.io/references.html)

[Previous page:](https://tguens.github.io/understand-predict-winner.github.io/resultsb.html)

[Back to main](https://tguens.github.io/understand-predict-winner.github.io/)
