#reading a csv file (practice from book)
read_csv("a,b,c
          1,2,3
         4,5,6")

#parsing a vector (wil take a character vector and return a more specialised vector like a logical, integer, or date)
str(parse_integer(c("1", "2", "3")))

parse_integer(c("1", "231", ".", "456"), na = ".")


parse_double("2.54")

#computation
table1 %>% 
   mutate(rate = cases / population * 100)
# A tibble: 6 x 5
country      year  cases population    rate
<chr>       <int>  <int>      <int>   <dbl>
  1 Afghanistan  1999    745   19987071 0.00373
2 Afghanistan  2000   2666   20595360 0.0129 
3 Brazil       1999  37737  172006362 0.0219 
4 Brazil       2000  80488  174504898 0.0461 
5 China        1999 212258 1272915272 0.0167 
6 China        2000 213766 1280428583 0.0167 

#plotting mpg via ggplot

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))

ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy, color = class))

