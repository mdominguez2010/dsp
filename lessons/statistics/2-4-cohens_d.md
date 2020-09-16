[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

def CohenEffectSize(group1, group2):
  diff  = group1.mean() - group2.mean()
    
  var1 = group1.var()
  var2 = group2.var()
  n1, n2 = len(group1), len(group2)
    
  pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
  d = diff / np.sqrt(pooled_var)
  return d
    
Let's create a dataframe filtering for first-borns only
firsts = live[live.birthord == 1]

Let's create another dataframe for all other babies
others = live[live.birthord != 1]

Calculate Cohen's Effect for weight in lbs
CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)

Cohen's d = -0.0887

Calculate Cohen's Effect for pregnancy length
CohenEffectSize(firsts.prglngth, others.prglngth)

Cohen's d = 0.0289

Differences in Cohen's Effects are small for both total weight and pregnancy length. However, the effect for weight is negative, while the effect for pregnancy length is positive.
