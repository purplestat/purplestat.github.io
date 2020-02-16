---
layout: post
title: "Robberies under the veil of darkness"
summary: "{I investigate how darkness affects the crime rates in chicago}"
keywords: "| visualisation, spatial"
---
In many TV-shows and crime movies, robberies predominantly take place during the late evening hours and happen often in shady and abandoned backalleys. I was wondering whether this hollywood depiction actually reassemlbes 
the truth or should rather be seen as a dramaturgic element since darkness is usually associated with the evil.
Despite this element, there are good reasons to believe that crime rates might changing troughout the day: For each robbery there needs to be an accessible victim. If everybody is asleep  On the one hand, 
since the criminal does not want to experience any interference of outsiders. On the other hand, the veil of darkness might help to approach a victim but also to vanish after the crime is done. 

The following two figures provide an overview of the location and historical development of robberies.
While Austin pretty noticable in it's number of robberies. Important to note that it's also one of the bigger areas that is densly populated.
<center>
<iframe src="https://rstudio-pubs-static.s3.amazonaws.com/565190_a675b3a64eed4b558a71d91683244ac9.html" style="border: none; width: 900px; height: 600px" scrolling="no"></iframe>
</center>
In gerneal, robberies seem to steadly declined over the last years. While the frequency of monthly robberies was around 1500 at the start of the century it decreased by roughly 50 percent to about 750 at the end of 2019. 
  <br> ![](https://github.com/purplestat/chicagocrime_code/blob/master/chicagocrime-notebook_files/figure-gfm/unnamed-chunk-10-3.png?raw=true?style=centerme)  
<br>
If you are particularily interested in this aspect you might want to have a look at a [report about the Chicago Police Department](https://abc7chicago.com/robberies-down-19-percent-citywide-in-2018-chicago-police-say/4974400/)
 and their strategic approach. However, I don't want to put too much emphasis on the general decline of robberies but rather focus on the cyclicality of robberies over the day. The subsequent graph shows the strong variation in robberies over the span of 24 hours. The frequency of robberies has it's low around 6am in the morning and increases steadily throught the day until the peak its around 9pm. The discrepancy is quite pronounced since the number of robberies at 6am is more than three times lower than at 9pm.
 
<br> ![](https://github.com/purplestat/chicagocrime_code/blob/master/chicagocrime-notebook_files/figure-gfm/unnamed-chunk-10-7.png?raw=true?style=centerme)  
<br>

The variation over time does no suffice to make any claim about the impact of darkness on robberies since the variation of crimes over the course of the day might be driven by various determinants. Especially working hours, leisure time and the associated movement of citizens outisde of their home can affect the prevalence of a crime. Fortunately, the sun provides a naturaly source of variation in length of day over the year. The following figure shows the changes in time of sunrise and -set throughtout a year.

  <br> ![](https://github.com/purplestat/chicagocrime_code/blob/master/chicagocrime-notebook_files/figure-gfm/unnamed-chunk-10-5.png?raw=true?style=centerme)  
<br>

A heatmap that depicts the frequency of robberies by time of the day and week of the year shows shifts that align with the previous graph: While the majority of robberies in winter happen in the hours approaching 8pm the corresponding time increases towards the sommer months and declines afterwards again. 

  <br> ![](https://github.com/purplestat/chicagocrime_code/blob/master/chicagocrime-notebook_files/figure-gfm/unnamed-chunk-10-1.png?raw=true?style=centerme)  
<br>

Normalizing the time of the crime as time until/after sunset shows this relationship even more explicitly. Right, after the sunset - during dawn - robberies steadily increase and seem to stabilize one hour thereafter at a noticably higher level.

  <br> ![](https://github.com/purplestat/chicagocrime_code/blob/master/chicagocrime-notebook_files/figure-gfm/unnamed-chunk-10-4.png?raw=true?style=centerme)  
<br>

Going one step further and looking into the variation of this correlation over weekdays shows that robberies shift more towards the hours after midnight. Since on the weekend more, possibly drunk people are on the streets at night they provide targets for robberies. 

  <br> ![](https://github.com/purplestat/chicagocrime_code/blob/master/chicagocrime-notebook_files/figure-gfm/unnamed-chunk-10-2.png?raw=true?style=centerme)  
<br>



[<a href="/blog">back</a>]
