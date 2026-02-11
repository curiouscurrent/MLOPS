We apply box-cox transform (for values strictly greater than 0) and Yeo-johnson transform(for both positive, negative, 0 values).  Performance of linear models improves greatly when it has normally distributed data, so we use these to get end output as normal distribution.

Log transform is applied on right skewed data,
Sq(x^2) transform is applied on left skewed data.

QQ plot is used for normal distributions, when the points are on the 45 degree line, it is normally distributed.


To encode numerical data, we use
1) Binning
2) Binarization

Why use it ? To handle outliers better, to improve the value spread (makes spread of data uniform)

Binning :
We use the class KBinsDiscretizer , with encoding as ordinal , 
strategy : uniform, quantile, kmeans.

Binarisation : 
Especially used in image processing 
we have to give a threshold
for example pixels : 0-255, so lets say threshold = 127.5 , 
any pixel value : 
< 127.5 -> 0, 
> 127.5 -> 1
