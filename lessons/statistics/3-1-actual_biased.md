[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

resp = nsfg.ReadFemResp()<br/>pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')<br/>thinkplot.Pmf(pmf)<br/>thinkplot.Config(xlabel='Household Size', ylabel='PMF')

def BiasPmf(pmf, label):<br/>
	new_pmf = pmf.Copy(label=label)

 	for x, p in pmf.Items():
   		new_pmf.Mult(x, x)
   
   	new_pmf.Normalize()
   		return new_pmf

biased_pmf = BiasPmf(pmf, label='biased')<br/>thinkplot.PrePlot(2)<br/>thinkplot.Pmfs([pmf, biased_pmf])<br/>thinkplot.Config(xlabel='Household Size', ylabel='PMF')

print('Actual mean', pmf.Mean())<br/>
	Actual mean 1.024205155043831

print('Observed mean', biased_pmf.Mean())<br/>
	Observed mean 2.403679100664282
