[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

    # Solution generate 1000 numbers
    np.random.random(1000)
    
    # Solution plot the PMF
    pmf = thinkstats2.Pmf(np.random.random(1000), label='random numbers')
    thinkplot.Pmf(pmf)
    thinkplot.Config(xlabel='number', ylabel='Pmf')
    
It's all bunched together. There is no clear way to distinguish any meaningful observations
    
    # Solution plot the CDF
    cdf = thinkstats2.Cdf(np.random.random(1000), label='random numbers')
    thinkplot.Cdf(cdf)
    thinkplot.Config(xlabel='number', ylabel='CDF', loc='upper left')
    
The distribution is in fact uniform
