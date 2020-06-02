[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

import thinkstats2<br/>
numbers = np.random.random(1000)<br/>
pmf = thinkstats2.Pmf(numbers)<br/>
thinkplot.Pmf(pmf,linewidth=0.1)<br/>
thinkplot.Config(xlabel='Random', ylabel='PMF')<br/>

There are too many values, each with a very low probability. This makes it difficult to draw any significant conclusions from the data.

cdf = thinkstats2.Cdf(numbers)<br/>
thinkplot.Cdf(cdf)<br/>
thinkplot.Configt(xlabel='Random', ylabel='CDF')<br/>

The distribution is uniform in the CDF plot.

