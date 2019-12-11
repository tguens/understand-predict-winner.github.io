## 4) Modeling approach

1) baseline models for comparison

Our baseline model is a logistic regression that predicts the results of each district. This model takes in input some social-economic predictors with general political information. We have trained this model in the results of the House of States elections from 2010 to 2016 and we tested this model on the 2018 elections. 

2) description of our implementations beyond baseline with design choices

    a) Part Théo + Will
    
    b) Predicting popular vote through polls
    
The aim is to infer the intention of votes at national scale and at all times during the campaign from polling data.
    
        i) Hidden States Model
Let's model the evolution of vote intention as a linear stochastic process. The intentions of vote at a nationnal scale are unknown, we can qualify them as latent variables or hidden states. We only have access to observations on a portion of the population at different times. These observations are the polls outcomes. With these polls, we want to determine the evolution of the intentions of votes and of its uncertainty.
    
We are making the following suppositions about the polls:
    - they all are reliable.
    - targeted people are drawn at random among the whole population of people who will vote.

Let's note $X_n = (R_n, D_n, O_n, U_n)$ the proportion of vote intention at a national scale at time $n$ (respectively percentage of Republian, Democrat, other and undecided votes). Let's note $Y_n = (r_n, d_n, o_n, u_n)$ the observations given by the poll at time $n$. Let's $p_n$ be the number of people asked for this poll.

The sample size of a poll is very tiny compare to the number of voters that has actually voted in 2018 (1,000 compare to 100,000,000), so we can model the poll as a sample with replacement. Hence the number of voters in each class follows a binomial. For example: $p_n r_n$ ~ $Bin(p_n, R_n)$, same for the 3 other classes. As $p_n >>1$ we can approximate the distribution by a normal, and suppose that it is continuous. The article [12] proves the convergence of a binomial to a normal. This approximation will be useful to predict the hidden states by using a Kalman filter.



        ii) Prediction with a Kalman filter
        
The Kalman filter is an algorithm widely used for estimating positions (e.g. GNSS applications). It gives a method to compute the hidden states, given two hypothesis:
- the process is linear
- the noises are gaussian.

I invite you to read this article if you are not familiar with this algorithm [13].

We can assimilate the process as a random walk, where at each step we add some white noise to the current state (we will tackle the fact the states percentages needs to some to one a bit later in this study). Hence the process is linear. The observation is the current state plus some white noise (because we approximate the binomial by a gaussian). Hence the hypothesis to use this algorithm stands.

Given all the observations we can predict all the past hidden states, this technic is called smoothing. We are using the package pykalman [14].

The algorithm works in two steps:
    - First it estimates the parameters of the linear gaussian process with the Expectation Maximisation algorithm
    - Then it computes the smoothed hidden states.
    
In order to simplify the problem, we used a different Kalman filter for each categories of vote. We lose the sum to one, but we would just have to renormalize them afterward (we will see that the sum of the smoothed proportions remain very close to one).
