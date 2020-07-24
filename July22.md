3. Provide a histogram of the probabilities for the logistic regression as well as your boosted tree model. How do you interpret the two different models? Are their predictions essentially the same or is there some area where they are noticeable different. Plot the probability density function of the resulting probability predictions from the two models and use them to further illustrate your argument. Include the ROC plot and interpret it with regard to the proportion of true to false positive rates, as well as the area under the ROC curve. How does the measure of the AUC reflect upon the predictive power of your model?

A1)One-hot-coded columns is a feature provided by feature columns that let's categorical variables be converted into a form that could be provided (numerical date) to machine learning algorithms to do a better job at predicting. The source values are discrete. 

A2) A dense feature inspects the result of a feature column and inspects categorical columns by transforming it to an indicator column first. This can be useful because it is another way to understand the data and give new meaning since certain values can't be interpreted correctly without it. 

A3)
![Unknown](https://user-images.githubusercontent.com/67920437/88332968-6fa38100-ccfd-11ea-84fc-25a596854a52.png)

![Unknown copy](https://user-images.githubusercontent.com/67920437/88333145-b5f8e000-ccfd-11ea-972d-a5be4a80ed12.png)

B1)

![Unknown copy 2](https://user-images.githubusercontent.com/67920437/88352271-3b44ba80-cd27-11ea-82d7-e8f8f05509c5.png)
![Unknown-2](https://user-images.githubusercontent.com/67920437/88352273-3bdd5100-cd27-11ea-8458-2641ed7cb2b0.png)

The features that contributed the most to the predicted probability are sex, age, and class. The graphs are showing that being a 31 year old male in 2nd class meant your chance of survival wasn't the best. The graphs also show that fare and parch made chances of survival better.  

B2)

![Unknown-3](https://user-images.githubusercontent.com/67920437/88352274-3bdd5100-cd27-11ea-8fd6-99e6bcd95cd9.png)
![Unknown-4](https://user-images.githubusercontent.com/67920437/88352275-3bdd5100-cd27-11ea-86ee-24e2657750e0.png)

The features that are the most important are sex, class, and age which makes sense. It was shown that women were favorable for survival and the more you paid for fare the higher of chance you had for survival, which basically means if you are 1st class that increased your chance. In the 2nd graph the red corresponds to larger function values (positive) and blue was smaller (negative). So the blue would mean the survival rate was low.  
