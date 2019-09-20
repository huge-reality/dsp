[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> rand_nums = np.random.random(1000)



>> pmf = thinkstats2.Pmf(rand_nums)

>> thinkplot.Pmf(pmf, linewidth=0.1)

>> thinkplot.Config(xlabel='variable', ylabel='probability')



>> cdf = thinkstats2.Cdf(rand_nums)

>> thinkplot.Cdf(cdf)

>> thinkplot.Config(xlabel='variable', ylabel='cumulative dist')

>>>> **Looking at the CDF, the distribution is not quite uniform, but pretty close. Presumably, with a larger amount of numbers generated, the distribution would get closer to uniformity.
