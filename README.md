# bin-width-in-R
Function to determine a good binwidth number for plotting histograms in R, ~~using the pracma library for the nthroot function~~ (now independent of any packages...calculating the nth root never really needed a package to begin with)
In cases in which the data has an intuitive binwidth (e.g. hours in a day plotted on the x axis), this function is not necessary.
However, in some data sets, it may be harder to determine a good starting point for a binwidth. Rather than tinkering with binwidths ad nauseum, this funciton finds a good *starting point* for your density plots and histograms. Why this formula? The idea was presented by Scott, 1979 "On optimal and data-based histograms" as a formula to achieve an unbiased estimation of binwidth. The formula is the following:
binwidth = 3.49 * sd *  N^(-1/3)
In other words, multiply 3.49 by the standard deviation and by the cubic root of the n()umber of observations.
