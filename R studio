1.Read the csv data file

LIFE_DATA=read.csv(file=file.choose(),header=TRUE)
2.Display head of data

 head(LIFE_DATA)
3.Display first n rows specified.

head(LIFE_DATA,n=10)
4.display tail of data

tail(LIFE_DATA)
5.Display n rows specified from bottom

tail(LIFE_DATA,n=10)
6.Determining type of data

class(LIFE_DATA)
7.Table command

table(LIFE_DATA$Entity)
table(LIFE_DATA$Year)
8.Determine the structure of data

str(LIFE_DATA)
9.Summarising the data

summary(LIFE_DATA)
10.Displaying length of year column

length(LIFE_DATA$Year)
11.Displaying Dimension of the data

dim(LIFE_DATA)
12.Displaying column names of data

colnames(LIFE_DATA)
13.Displaying type of some datastructure in the data

typeof(LIFE_DATA$Year)
14.list of variables present in life expectancy data

ls(LIFE_DATA)
15.Display 1st row and all columns of dataframe

LIFE_DATA[1,]
16.Display all rows and 1st columns of dataframe

LIFE_DATA[,1]
17.Dispalying data in 2nd row and 3rd column of the data frame

LIFE_DATA[2,3]
18.Displaying 1st and 2nd row and all columns

LIFE_DATA[1:2,]
19.Displaying all rows and first 3 columns

LIFE_DATA[,3]
20.Selecting data where Entity name is Australia with subset operator

temp_data=subset(LIFE_DATA,Entity=="Australia")
temp_data
Displaying sum of life expectancy column
sum(LIFE_DATA[3])
Display the maximun value of the life expectancy column
max(LIFE_DATA[3])
Display the minimum value of the life expectancy column
min(LIFE_DATA[3])
24.Attaching life expectanct data

attach(LIFE_DATA)
25.Now we use variables inside life data

min(Life.expectancy)
tail(Year)
26.Sorting Life expectancy variable in ascending order

sort(Life.expectancy)
27.Sorting Life expectancy variable in descending order

sort(Life.expectancy,decreasing=TRUE)
28.Detaching life data

detach(LIFE_DATA)
29.Using with operator to use variables inside data

with(LIFE_DATA,Life.expectancy)
30.Finding median of data

median(LIFE_DATA$Life.expectancy)
       
Finding mean of data
mean(LIFE_DATA$Life.expectancy
     )
32.Finding standard deviation of data

sd(LIFE_DATA$Life.expectancy)
33.Finding variance of data

var(LIFE_DATA$Life.expectancy)
34.order the life expectancy column in ascending order

order(LIFE_DATA[3])
35.order the life expectancy column in descending order

order(LIFE_DATA$Life.expectancy,decreasing = TRUE)
36.Rank of Year column

rank(LIFE_DATA$Year)
37.Rank of year column with average as tie breaker

rank(LIFE_DATA$Year,ties.method= "average")
DPLYR operations

38.Usage of mutate function

library(dplyr)

head(LIFE_DATA %>%mutate(mutatrd_Life.expectancy=Life.expectancy-mean(Life.expectancy)))
39.Summarise function

head(LIFE_DATA %>% group_by(Year,Entity) %>% summarise(weight_Life.expectancy=mean(Life.expectancy)))
40.Rename operation

copy_life=LIFE_DATA
pd_mod <- copy_life %>% rename(renamed_Life.expectancy = Life.expectancy)
head(pd_mod)
Selecting specific columns
copy_life=LIFE_DATA
copy_life %>% select(Entity,Year)
Reordering of columns using select function
copy_life=LIFE_DATA
copy_life %>% select(Entity,Life.expectancy)
Filter command
copy_life=LIFE_DATA
copy_life %>% filter(Life.expectancy >=31 & Life.expectancy <=55)
44.Histogram

library(ggplot2)
ggplot(LIFE_DATA, aes(x=Life.expectancy)) +geom_histogram()
        
45.Histogram of Life expectancy column and its density

ggplot(LIFE_DATA,aes(x=Life.expectancy))+ geom_histogram(fill="cornsilk",color="blue",size=0.2)+geom_density(color="black")
46.Line graph of Life.expectancy column and its density

ggplot(LIFE_DATA,aes(x=Life.expectancy))+geom_density(fill="blue",alpha=.4)
47.Dot plot

library(ggplot2)
ggplot(LIFE_DATA,aes(x=Year,y=Life.expectancy))+geom_dotplot(binaxis="y",stackdir="center",binwidth = 4,fill="green")
48.Box plot

ggplot(LIFE_DATA,aes(x=Year,y=Life.expectancy))+geom_boxplot(width = 0.1,fill="black")+stat_summary(func='median',fill="white",shape=21)
49.Density plot for year and life expectancy

library(ggplot2)
ggplot(LIFE_DATA,aes(x=Year,y=Life.expectancy))+geom_density2d(aes(colour=..level..))

50.violin plot

Year and life expectancy

ggplot(LIFE_DATA,aes(x=Year,y=Life.expectancy))+geom_violin()
