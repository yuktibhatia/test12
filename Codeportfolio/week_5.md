#Quiz
library (yarrr)
#matrix
matrix(1:9,nrow=3, ncol = 3)

#vectorization

a <- c(2,3,4)
b <- c(20,30,40)
(a+b) / 10
[1] 2.2 3.3 4.4

# tidy data - Converts data to tbl class. tbl’s are easier to examine than data frames. 
dplyr::glimpse(iris)
# Information dense summary of tbl data. 

View(iris)

%>% 
  iris %>%
  group_by(Species) %>%
  summarise(avg = mean(Sepal.Width)) %>%
  arrange(avg)
#Passes object on lef hand side as first argument of function on righthand side. (with group by, summarise and average)


