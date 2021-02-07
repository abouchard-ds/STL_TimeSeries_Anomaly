# STL_TimeSeries_Anomaly
Implementation of an anomaly detection algorithm using "Seasonal and Trend decomposition using Loess".

# Research

**Original paper**:
http://www.nniiem.ru/file/news/2016/stl-statistical-model.pdf

https://ojs.aaai.org/index.php/AAAI/article/view/4480/4358

https://otexts.com/fpp2/stl.html

https://en.wikipedia.org/wiki/Decomposition_of_time_series

https://towardsdatascience.com/stl-decomposition-how-to-do-it-from-scratch-b686711986ec

** Python Library**:
https://www.statsmodels.org/stable/examples/notebooks/generated/stl_decomposition.html



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


