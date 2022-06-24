# Bloc_3-Projet_Walmart_Sales

## Project's presentation 🎥
https://share.vidyard.com/watch/qob8NzyzYfPX2ypFasArZr?![image](https://user-images.githubusercontent.com/94960539/175549998-5b85fc30-0355-4aba-9c45-776fdfdabf9c.png)


## Goals 🎯
* Walmart's marketing service wants to estimate / to forecast their weekly sales.
* To achieve / answer this goal, a machine learning model will be build, with the best precision possible on the predictions made.
* Such a model would help the team understand better how the sales are influenced by economic indicators, and might be used to plan future marketing campaigns.
* As the objective is to predict continuous quantitative data, a multiple linear regression model will be built and optimized.

## Key take away 📬
* The model is just above a "dummy" model (on training set) and is slightly overfitting... Our model, based on macro-economic features, is clearly not able to predict correctly the weekly sales: only 11.6% of the variability in sales explained (R2), and huge average forecast's distance from true value (MAE) of 549786 dollars (more of less vs true value).
Among the economic/macro-environment factors, the Consumer Price Index (CPI) seems the one with the stronger influence on the sales, followed by Temperature and Unemployment Rate.

* With the Ridge optimization, we do not have an improvement of our model: the R2 remains quite stable 10.2% with Ridge optimization vs 11.6% without Ridge optimization.

* Running a model with only macro-economics features is not efficient, the model is not good for making predictions (too high errors). Next steps is to improve the model by adding, at least, the "Month" feature as it show some "common" trends. Indeed, the model quality improves with a R2 of 37% on training set and 34% on test set.

* Our model, do not include the "Store" feature as the data "quality" is quite different from one store to another (some stores have 10 or more weeks of data vs other with only three weeks). Moreover, the sales are 'only' done through the "Store" channel, that would be interesting to add this "channel" feature if we could have "Store" channel and "Online" channel.
