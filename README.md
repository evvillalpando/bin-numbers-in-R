# bin-width-in-R
Function to determine a good binwidth number for plotting histograms in R, using the pracma library for the nthroot function.
In some cases in which the data lends to an intuitive binwidth (e.g. time plotted on the x axis), one should always go with that.
However, in some data sets, it may be harder to determine a good starting point for a binwidth. Rather than tinkering with binwidths ad nauseum, this funciton finds a good *starting point* for your density plots and histograms. Why this formula? The idea was presented by Scott, 1979 "On optimal and data-based histograms" as a formula to achieve an unbiased estimation of binwidth. The formula is the following:
binwidth = 3.49 * sd *  N^(-1/3)
In other words, multiply 3.49 by the standard deviation and by the cubic root of the n()umber of observations.
