[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

    # Solution actual distribution
    pmf = thinkstats2.Pmf(resp.numkdhh, label='number of children')
    
    # Solution plot of actual distribution
    thinkplot.Pmf(pmf)
    thinkplot.Config(xlabel='number of children', ylabel='Pmf')
    
    # Solution computing biased distribution
    def BiasPmf(pmf, label):
        new_pmf = pmf.Copy(label=label)
    
        for x, p in pmf.Items():
            new_pmf.Mult(x, x)
    
        new_pmf.Normalize()
        return new_pmf

    biased_pmf = BiasPmf(pmf, label='biased')

    # Solution plotting  the actual vs the biased distributions
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biased_pmf])
    thinkplot.Config(xlabel='number of children', ylabel='PMF')
    
    # Solution computing mean of actual distribution
    pmf.Mean()
    
    # Solution computing the mean of biased distribution
    biased_pmf.Mean()
