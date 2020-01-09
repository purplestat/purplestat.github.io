---
layout: post
title: "What makes candy popular?"
summary: "An analysis of candy components and their popularity"
---

I really enjoyed reading the “Ultimate Halloween Candy Power Ranking” by
[FiveThirtyEight](https://fivethirtyeight.com/features/the-ultimate-halloween-candy-power-ranking/).
They made use of an online survey in which people had to choose their
preferred candy based on two randomly offered options (out of 85
possible products). Based on a decently sized sample FiveThirtyEight
tried to infer the ingredients that led to the popularity. Even though
their investigation provides nice insights, I had the impression that
their analysis could be further enriched by incorporating the
interaction between ingredients. While Chocolate and Ketchup might be
popular on their own, mixing those ingredients is rather unlikely to be
very successful.  
Each product is categorised by six non exclusive taste components:
*chocolate*, *fruit*, *nut*, *nougat*, *caramel* and *crunch*. Morever,
five additional characteristica are employed: The *relative amount of
sugar*, the *relative price* and indcator capturing if a candy is
*hard*, a *bar* or *included in a package* with other candy. The violin
plots in the figure below show the popularity distribution across those
components. The median popularity is captured by the red dot while the
dashed line provides the average popularity across all products.


  <br> ![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-8-1.png?raw=true?style=centerme)  
<br>



Especially candy that contains a chocolate, nut or crunch component
appears the be very popular. However, this isolated perspective is not
sufficient to identify the underlying driver of success since the
components are non-exclusive. The subsequent figure shows the
correlation between the characteristica and therefore the tendency that
some components are rather often combined.

![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-5-1.png?raw=true?style=centerme)

While the combination between chocolate and fruit is rather unusual the
combination between chocolate and nut occurs more often. The partial
impact of the components is investigated by means of an ordinarly least
squares estimation. The following graph shows the point estimates and
the corresponding 95% confidence intervals.

<br> ![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-15-1.png?raw=true?style=centerme) <br>

Chocolate appears to be the strongest driver of popularity, while fruit,
crunch and nut seem to have a moderatly positive effect as well. As
reference group serves candy without any of the mentioned components.  
Under the assumption that the components are additively seperable we
could stop the analysis at this point. However, since it’s unlikely that
all ingredients assort well will each other we need to have a look at
the interactions as well. If we focus on the six taste components there
is a total of 2^6=64 possible combinations. In our sample on 16 of those
different combinations actually exist. The following list shows the
grouped pairings ranked by their average popularity.

<br> ![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-12-1.png?raw=true?style=centerme) <br>

The list provides a few valuable insights: (**1**) All successful candy
contains a chocolate component; (**2**) The majority of candy contains
either chocolate or fruit, but there is only a single product with both
ingredients; (**3**) candy with caramel or nuts is not particular
popular unless it contains a chocolate component as well.  
Even though candy containing chocolate is very popular, pure chocolate
products have only an average rating. The following graph contrasts
popularity and the number of taste components. People tend to value more
complex taste combinations.

<br> ![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-10-1.png?raw=true?style=centerme) <br>

Moreover, the amount of sugar also seems to be a driving factor.

<br> ![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-9-1.png?raw=true?style=centerme) <br>

Since the number of possible interactions is pretty large and the number
of different products and the respective combination of components is
fairly small the estimation is constrained by the power of the data.
Allowing for too much flexibility raises the problem that estimates are
based on few products and more prone to be biased by brand specific
effects that are not reflected by the ingredients. On the other hand,
the incorporation of too few interactions neglects the importance of
pairing suitable ingredients. To account for both of those dimensions I
use the information of the previous table and focus in particular on the
interaction between chocolate and other ingredients.  


<br> ![](https://github.com/purplestat/candy_code/blob/master/candy-notebook_files/figure-gfm/unnamed-chunk-19-1.png?raw=true?style=centerme) <br>


The interaction between chocolate \* nut and chocolate \* caramel
appears to be an important determinant for the popularity of chocolate
products. The crunch component seems to be also imporant in this regard.
However, while the interaction between caramel \* crunch has no
significant effect, the combination of nut with either caramel or or
crunch seems have an adverse effect on popularity. Consequently, the
combinations of choice would be Chocolate-Caramel-Crunch or
Chocolate-Nut. This is also in line with the ranking of the previous
table.

[<a href="/blog">back</a>]
