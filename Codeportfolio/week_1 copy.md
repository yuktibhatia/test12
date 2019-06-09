#Basic practice
> print(cat)
function (..., file = "", sep = " ", fill = FALSE, labels = NULL, 
          append = FALSE) 
{
  if (is.character(file)) 
    if (file == "") 
      file <- stdout()
    else if (substring(file, 1L, 1L) == "|") {
      file <- pipe(substring(file, 2L), "w")
      on.exit(close(file))
    }
    else {
      file <- file(file, ifelse(append, "a", "w"))
      on.exit(close(file))
    }
    .Internal(cat(list(...), file, sep, fill, labels, append))
}
<environment: namespace:base>
  
#Square
Square <- function(x) {
  return(x^2)
}

print(Square(4))
print(Square(x=4)) # same thing
[1] 16
[1] 16

#Lists
sum(0:9)
append(LETTERS[1:13],letters[14:26])
c(1,6,4,9)*2
something <- c(1,4,letters[2])  # indices start at one, you get (1,4,"b")
length(something)

#seq function
seq(from=1,to=4,by=.6)

#Reading user input
readinteger <- function()
{ 
  n <- readline(prompt="Enter an integer: ")
  return(as.integer(n))
}

print(readinteger())

#Rounding
> round(22.5,0)  # rounds to even number
[1] 22
> round(3.14,1)
[1] 3.1

#Reading data
tbl <- read.table(file.choose(),header=TRUE,sep=",")
population <- tbl["POPESTIMATE2009"]
print(summary(population[-1:-5,]))

#Indexing data frames
tbl["POPESTIMATE2009"]:
  
#Fetching specific rows and columns
population[1:5,]  #  first the rows, then the columns

#Summary function
summary(1:10)

#Filtering Data
tbl <- read.table(file.choose(),header=TRUE,sep=',')
population <- tbl[c("NAME","POPESTIMATE2009","NPOPCHG_2009")]
smallest.state.pop <- min(population$POPESTIMATE2009)
print(population[population$POPESTIMATE2009==smallest.state.pop,])

#Finding data sources
mtcars
print(head(mtcars))

#Matrix
print(matrix(runif(6*3), nrow=6, ncol=3))
