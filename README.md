# STL_TimeSeries_Anomaly
Implementation of an anomaly detection algorithm using "Seasonal and Trend decomposition using Loess".

# Research

Research papers:

Cleveland RB, Cleveland WS, McRae JE, Terpenning I. STL: A seasonal-trend decomposition. Journal of official statistics. 1990;6(1):3-73.
- **Original paper**: http://www.nniiem.ru/file/news/2016/stl-statistical-model.pdf

Wen Q, Gao J, Song X, Sun L, Xu H, Zhu S. RobustSTL: A robust seasonal-trend decomposition algorithm for long time series. InProceedings of the AAAI Conference on Artificial Intelligence 2019 Jul 17 (Vol. 33, No. 01, pp. 5409-5416).
- Improvement: https://ojs.aaai.org/index.php/AAAI/article/view/4480/4358

https://www.google.com/url?q=http://scholar.google.ca/scholar%3Fq%3Dseasonal-trend%2Bdecomposition%26hl%3Den%26as_sdt%3D0%26as_vis%3D1%26oi%3Dscholart&sa=U&ved=2ahUKEwjM05X8m9buAhXxm-AKHRA_BSAQgQN6BAgLEAE&usg=AOvVaw3LNqnH2Ggwh8BRsnkKxW-2

Wonderful book: 
- https://otexts.com/fpp2/stl.html
- https://otexts.com/fpp2/forecasting-decomposition.html
- https://otexts.com/fpp2/stationarity.html

General concepts:
- https://en.wikipedia.org/wiki/Decomposition_of_time_series



**Python Library**:
https://www.statsmodels.org/stable/examples/notebooks/generated/stl_decomposition.html

https://blog.statsbot.co/time-series-anomaly-detection-algorithms-1cef5519aef2


Low quality articles but still help:
- This is **not from scratch** at all: https://towardsdatascience.com/stl-decomposition-how-to-do-it-from-scratch-b686711986ec
- https://stats.stackexchange.com/questions/298560/is-stl-a-good-technique-for-forecasting-instead-of-arima
- https://stats.stackexchange.com/questions/298560/is-stl-a-good-technique-for-forecasting-instead-of-arima


Videos:
- https://youtu.be/DZ403FNW2YI
- https://youtu.be/1NXryMoU7Ho
- https://youtu.be/mG4ZpEhRKHA


## Seasonal-Trend decomposition
STL find the trend and seasonality and take the residual from the raw data versus the model.

```math
Raw_data - (trend + seasonnality) = residual
```

- Can use the residual to find anomalies (datapoints that are not explained by the trend and seasonality);
- Can use trend and seasonnality to forecast futur behavior;

## Loess:

Loess regression is a **nonparametric** technique that uses *local weighted* regression to fit a smooth curve through points in a scatter plot. Loess curves can reveal trends and cycles in data that might be difficult to model with a parametric curve.

It is a generalization of moving average and polynomial regression.

Requires fairly large, densely sampled data sets in order to produce good models. (a cause de l'utilisation de k-nn)

Prone to the effects of outliers in the data set, like other least squares methods. (si ca fait trop longtemps qu'on a une situation anormale, il va la trouvee normale)

https://en.wikipedia.org/wiki/Local_regression


