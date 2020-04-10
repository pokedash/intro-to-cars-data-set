# intro-to-cars-data-set

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Introduction to Cars
This is an introduction to `cars` dataset. The data given is a comperison to speed and distants.

```data.set=cars
data(cars)
```

# Histograms

# Speed

we will begin by making a histogram. As you can see the average speed is 10-20
```{r}
hist(cars$speed, col="blue")
```

# Distances
this is another Histogram but for distance adn as we can see from the information given the average distance traveled is 20-40 km
```{r}
hist(cars$dist, col="Red")
```
# Boxplot

# Speed
this is the information but as a boxplot. as we can clearly see the average is 15
```{r}
boxplot(cars$speed, col = "GREEN")
```
# Distance
hear we can see the exact same like on the other diagram the average is 30
```{r}
boxplot(cars$dist, col = "PINK")
```
# scaterplot
this is a scatterblock diagram and it is comparing both of the values, speed and distance. as we can see the lines are going higher, which means that the more the speed, the more the distance and vice verca. 

```{r}
plot(x=cars$speed, y=cars$dist, main="Cras comparision to speed and distance", col="PURPLE")
lin.mod <- lm(cars$dist~cars$speed)
pr.lm <- predict(lin.mod)
lines(pr.lm~cars$speed, col="blue", lwd=0.7)
```
