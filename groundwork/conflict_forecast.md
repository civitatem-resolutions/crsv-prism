# [Conflict Forecast](https://conflictforecast.org/)

The **Conflict Forecast** by the WFP is a digital tool that predicts armed conflict and disruptive events like protests and riots. It integrates multiple conflict datasets with socio-economic, population density and critical infrastructure data to visualize conflict events and predict access disruptions.

### Drawbacks:
- The tool focuses almost exclusively on conflicts that are already underway or have recently ended.
- **Food for Thought**: Could it be that western countries like that US have such low conflict forecast despite what's going on there, because the model they've built has been that biased? Need to research about the building of the Conflict Forecast in greater detail.

### Some More Study Material

- [The Hard Problem of Prediction for Conflict Prevention](https://academic.oup.com/jeea/article/20/6/2440/6574413)
    - Project summarizes over four million newspaper articles using a topic model, the topics are then fed into a random forest to predict conflict risk, which is then integrated in a simple static framework in which a decision maker decides on the optimal number of interventions to minimize the total cost of conflict and intervention.
    - A key challenge of conflict forecasting is that **outbreaks in previously peaceful countries are hard to predict**.
- Using Past Violence and Current News to Predict Changes in Violence
- Reading Between the Lines: Prediction of Political Violence Using Newspaper Text
    - Through machine learning, vast quantities of newspaper text are reduced to interpretable topics. These topics are then used in panel regressions to predict the onset of conflict.
    - It is important to make distinctions for between-country and within-country variations:
        - Factors that contribute to conflict vary more between countries than within countries over time
        - Forecasting the timing of armed conflict is difficult since it is both rare and relatively concentrated in some countries; the variation between countries can dominate analysis
    - It is easier to predict whether a country is at rish *in general* rather then *when* a country is particularly at risk.

### Topic Modelling and How They've Helped So Far

> ... we implement an automated method to quantify the content of news using the **latent Dirichlet allocation (LDA)** model, which we apply to over 700,000 newspaper articles from English-speaking newspapers.

Topics provide depth because they put words into context, which can be useful for forecasting. They provide width too, because they allow for the usage of the whole text, including stabilizing factors, when forecasting conflict.

### Implementation Details

- Panel Regression Model that uses generated topics as explanatory variables
- Latent Dirichlet Allocation (LDA)

**3-Step Empirical Methodology**
1. Download newspaper articles and collect words and series of words (tokens) in one vector for each article
2. Develop a topic model tailoed for the purpose of summarizing the content of news reports in a country and year using LDA for quantitative summaries
3. Use the within-country variation (emergence and disappearance of topics on the country level) to predict conflic out of sample. 

### Stray Thoughts

the paradox of stereotyping is that we train our models on historical data, we train it to have bias, and we advocate for unbiased views while all the predictions we make are based on the past;we train it to have bias;

our ml runs on the belief that we are unlikely to learn from our mistakes; that's what our conflict forecast models believe in, which is why they find it so difficult to predict if an outbreak will come out in a previously peaceful country; then again, all countries were peaceful before they had their first outbreak

more about stereotyping; "The paradox of stereotyping and disapproval", axel arturo barcelo aspeitia

also, the white savior complex? the white superiority complex? does it manifest itself in conflict research?