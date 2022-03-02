# geom\_point

```
ggplot(gapminder, 
aes(x=gdpPercap, y=lifeExp, color=continent)) +
geom_point() + geom_smooth(method='loess', formula='y~x') +
facet_wrap(~continent)
```

![](<../.gitbook/assets/image (21).png>)

For smooth graphs
