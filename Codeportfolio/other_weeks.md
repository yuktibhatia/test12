#boxplot
boxplot(pollution$pm25, col = "blue")
abline(h = 12)

#histogram
hist(pollution$pm25, col = "green")

#barplot
table(pollution$region) %>% barplot(col = "green")

#multiple boxplot
boxplot(pm25 ~ region, data = pollution, col = "green")

#multiple histogram
par(mfrow = c(2, 1), mar = c(4, 4, 2, 1))
> hist(subset(pollution, region == "east")$pm25, col = "green")
> hist(subset(pollution, region == "west")$pm25, col = "green")

#scatterplot
with(pollution, plot(latitude, pm25))
> abline(h = 12, lwd = 2, lty = 2)

#Multiple Scatterplots
> par(mfrow = c(1, 2), mar = c(5, 4, 2, 1))
> with(subset(pollution, region == "west"), plot(latitude, pm25, main = "West"))
> with(subset(pollution, region == "east"), plot(latitude, pm25, main = "East")
       
#base plotting system
data(airquality)
> with(airquality, {
  +         plot(Temp, Ozone)
  +         lines(loess.smooth(Temp, Ozone))
  + })

## Add annotation
> title("Speed vs. Stopping distance")
