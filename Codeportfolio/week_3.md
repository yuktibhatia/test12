#sort (sorting data by height)
pirates <- pirates[order(pirates$height),]

#looking at few rows and coloumns 
ozone[1:5, 1:4]

# Sort the pirates dataframe by sex and then height
pirates <- pirates[order(pirates$sex, pirates$height),]

#Combing data (practice merge function)
combined.survey <- merge(x = survey.a,
                         y = survey.b,
                         by = "coloumn1",
                         all = TRUE)
# Print results
combined.survey

# Create a vector. 
x <- c(12,7,3,4.2,18,2,54,-21,8,-5)

# Find Mean.
result.mean <- mean(x)
print(result.mean)
[1] 8.22

#long_name function
long_name <- function(a = "a_long_argument" ,
                      
                      b = "another_argument",
                      
                      c = "another_long_argument)

