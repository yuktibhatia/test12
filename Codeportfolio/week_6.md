str(iris)
#Get a summary of an object’s structure.

class(iris)
#Find the class an object belongs to.

install.packages(‘dplyr’)
#Download and install a package from CRAN.

library(dplyr)
#Load the package into the session, making all its functions available to use. 

data(iris)
#Load a build-in dataset into the environment. 

#Reading & writing data
df <- read.table(‘file.txt’)
write.table(df, ‘file.txt’) 

#Remove x from the dataset
rm(x)

#Remove all variables from the environment
rm(list = ls()) 

#functions
> x <- c(1,2,3,4,5,6)
> var(x)
[1] 3.5
> sd(x)
[1] 1.870829
> log(x)
[1] 0.0000000 0.6931472 1.0986123 1.3862944 1.6094379 1.7917595
> max(x)
[1] 6
> round(x, 2)
[1] 1 2 3 4 5 6
> sum(x)
[1] 21
> median(x)
[1] 3.5
> quantile(x)
0%  25%  50%  75% 100% 
1.00 2.25 3.50 4.75 6.00 
> rank(x)
[1] 1 2 3 4 5 6


