#working directory
getwd()
[1] "/Users/yuktibhatia"

#Read file
read.table(file = "mydata.txt", sep, header)

#changing working directory
setwd(dir = "/Users/yuktibhatia/Dropbox/DataVis"
      
#Remeove all objects from workspace
rm(list = ls())

#data frame
data.frame("day" = c("mon", "fri", "sun"),
           "time" = c(8, 12, 16),
           "passengers" = c("16", "24", "56"))

#mean
mean ("Sample Duration")
#for US EPA AirData - Sample Duration coloumn

#check the number of rows and columns
nrow(ozone)
ncol(ozone)

#Running str() - gives reasonable output for any R object
str(ozone)

#Find Top and Bottom data
head(ozone[, c(8:9, 10)])
tail(ozone[, c(8:9, 10)])

#Practiced "filter" function from notes
filter(ozone, State.Code == "36" 
             & County.Code == "033" 
              & Date.Local == "2014-09-30") %>%
            select(Date.Local, Time.Local, 
            Sample.Measurement) %>% 
            as.data.frame
Date.Local Time.Local Sample.Measurement

#Ranking for ozone data
head(ranking, 10)



