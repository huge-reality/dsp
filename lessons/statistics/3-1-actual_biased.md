[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> resp = nsfg.ReadFemResp()

>> pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')

>> thinkplot.Config(xlabel='Number of children', ylabel='PMF')

>> def BiasPmf(pmf, label):

>>>> new_pmf = pmf.Copy(label=label)
    
>>>> for x, p in pmf.Items():
    
>>>>>>new_pmf.Mult(x, x)
        
        
>>>> new_pmf.Normalize()
    
>>>> return new_pmf
   
>> biased = BiasPmf(pmf, label='biased')

>> thinkplot.PrePlot(2)

>> thinkplot.Pmfs([pmf, biased])

>> thinkplot.Config(xlabel='Number of children', ylabel='PMF')

>> pmf.Mean()

>>>> 1.024205155043831

>> biased.Mean()

>>>> 2.403679100664282



>> **If you asked children how many children were in their family, you would get a biased response because children from large families would be more likely to respond, and families with no children would not get a chance to respond at all. The biased sample yields a mean of 2.4 children per family, as compared to the actual mean of 1.02 children per family.
