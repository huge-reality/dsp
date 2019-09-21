[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> **34%**

>> scipy.stats.norm can construct a normal distribution with a mean of 178 and a standard deviation of 7.7 as follows:

>>>> norm_dist = scipy.stats.norm(loc = 178, scale = 7.7)

>> using a cdf you can find out what percentage of men are too short, too tall, and in the right range like this (after converting the range to centimeters):

>>>> too_short = norm_dist.cdf(177.8)

>>>> too_tall = 1 - norm_dist.cdf(185.4)

>>>> too_short, too_tall, 1 - (too_short + too_tall)

>>>> (0.48963902786483265, 0.16826628918921427, 0.342094682945953)
