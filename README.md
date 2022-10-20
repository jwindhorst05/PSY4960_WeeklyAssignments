# PSY4960_WeeklyAssignments
title: "Quiz 1"
author: "Amanda Mae Woodward"
date: "2022-10-11"
output: html_document
---
This quiz will cover everything we've covered in Base R. 
1. Open the tidyverse library.
library(tidyverse)
2. Open the starwars dataset.
data(starwars)
3. Create a subset of data that contains only the humans from the starwars franchise.
humanstarwars<-subset(starwars,starwars$species=="Human")
4. In this subset of data, who is the tallest character? 
humanstarwars[which.max(humanstarwars$height),]
or summary(humans$height)
5. In this subset of data, print the information about the character in the third row. 
humanstarwars[3,]
6. In the full starwars dataset, calculate the average mass for the masculine characters. 
massmasc<-(data.frame(starwars %>% filter(gender=="masculine") %>% select(mass)))
> mean(massmasc %>% select(mass))
7. Create a dataset that contains only the characters and the films that they appeared in from the full dataset. 
filmcharstarwars<-subset(starwars, select = c("name", "films"))
8. Create a new column in the starwars dataset that contains a "ranking" of all characters (Note: you don't have to actually rank them. Just fill the column in with the numbers 1-87)
starwars$ranking<-NA
starwars$ranking<-1:87
9. Create a subset of data for the characters from Naboo. How many characters are from Naboo? 
starwars<-subset(starwars,starwars$homeworld=="Naboo") nrow(starwarsNab)
10. How many droids are in the full dataset? 
nrow(starwars$species=="Droid")
