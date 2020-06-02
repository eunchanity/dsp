[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

import scipy.stats<br/>
mean = 178<br/>
std = 7.7<br/>
dist = scipy.stats.norm(loc=mean, scale=std)<br/>

low = dist.cdf(177.8)<br/>
high = dist.cdf(185.4)<br/>
low-high<br/>

	Around 34.2% of US males are between 5'10" and 6'1"