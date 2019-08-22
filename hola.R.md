```{r}
competitions_per_golfer <- sapply(unique(data$GolferID),
                                  function(x) length(unique(data$Week[data$GolferID==x])))
round(table(competitions_per_golfer)/length(competitions_per_golfer)*100, 2)
hist(competitions_per_golfer)
```
