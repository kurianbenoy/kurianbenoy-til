---
description: ramblings on using ggplot
---

# Facet\_grid and Facet\_wrap

How to create wonderful visualizations in R like the below with multiple panel plots?

![](<../.gitbook/assets/image (16).png>)

Facetting - can be consider as a method to create multiple panel plots based on splitting attributes which we decide.



![](<../.gitbook/assets/image (15) (1).png>)

**Using facet\_grid**

****

```
ggplot(gapminder, aes(x=continent, y=gdpPercap))
 + geom_bar(stat = 'identity', fill='forest green')
   + facet_wrap(~year)
```

![](<../.gitbook/assets/image (18).png>)



**Using facet\_wrap**



```
ggplot(gapminder, aes(x=pop)) + geom_density() +
 facet_wrap(~year) + scale_x_log10()
```

![](<../.gitbook/assets/image (19).png>)

**Main difference I noticed was:**

\*facet\_wrap\* was working only for a single varaibles, but to create a multple plot in two dimension we had to used \*facet-grid\*



**Reference**



{% embed url="https://www.datacamp.com/community/tutorials/facets-ggplot-r" %}

Dr Ebin Sir's tidverse tutorials

