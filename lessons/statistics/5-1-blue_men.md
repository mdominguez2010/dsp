[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

    # Solution
    # First, let's convert feet to centimeters for consistency

    lower_bound_in = 70
    upper_bound_in = 73

    lower_bound_cm = round(lower_bound_in * 2.54, 1)
    upper_bound_cm = round(upper_bound_in * 2.54, 1)
    
    # The following are the lower and upper bounds in cm

    lower_bound_cm, upper_bound_cm
    
    # Evaluate CDFs

    print(dist.cdf(lower_bound_cm))
    print(dist.cdf(upper_bound_cm))
    print(dist.cdf(upper_bound_cm) - dist.cdf(lower_bound_cm))
    
Approximately 49% of the male population is 5'10" or shorter. About 83% of the population is 6'1" or shorter. And about 34% of the population is between 5'10" and 6'1"    
    
