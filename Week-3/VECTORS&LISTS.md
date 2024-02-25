#WEEK-3
#TASK-1(VECTORS&LISTS)
#Q-1
> rev_vector <- c("a", "b", "c", "d", "e")
> rev_vector <- rev_vector[5:1]
> rev_vector
[1] "e" "d" "c" "b" "a"

#Q-2
>vector1 <- c("THIS", "is", "MY")
>vector2 <- c("FIRST" ,"R", "PROGRAMME")
>cat(vector1,vector2)
THIS is MY FIRST R PROGRAMME


#Q-3
> v = c(0, 10, 20, 30, 40, 50, 60, 70, 80, 90)
> cnt =  sum(v > 10 & v < 70)
> print(cnt)
5

#Q-4
> v1= c(0, 10, 20, 30, 40)
> v2= c(50, 60, 70, 80, 90)
> row=rbind(v1,v2)
> column=cbind(v1,v2)
> print(row)
   [,1] [,2] [,3] [,4] [,5]
v1    0   10   20   30   40
v2   50   60   70   80   90
> print(column)
     v1 v2
[1,]  0 50
[2,] 10 60
[3,] 20 70
[4,] 30 80
[5,] 40 90

#Q-5
> v<-c(50,6,22,39,1,25,3)
> print(v>10)
[1]  TRUE FALSE  TRUE  TRUE FALSE  TRUE FALSE

#Q-6
> list= list("Python", "R", c(5, 7, 9, 11), TRUE, 144.76, "=","+","-")
> print(list)
[[1]]
[1] "Python"

[[2]]
[1] "R"

[[3]]
[1]  5  7  9 11

[[4]]
[1] TRUE

[[5]]
[1] 144.76

[[6]]
[1] "="

[[7]]
[1] "+"

[[8]]
[1] "-"

#Q-7
> list <- list(c("Red","Green","Black"), matrix(c(1,3,5,7,9,11), nrow = 2),list("Python", "PHP", "Java"))
> print(list)
[[1]]
[1] "Red"   "Green" "Black"

[[2]]
     [,1] [,2] [,3]
[1,]    1    5    9
[2,]    3    7   11

[[3]]
[[3]][[1]]
[1] "Python"

[[3]][[2]]
[1] "PHP"

[[3]][[3]]
[1] "Java"

> print(list[1])
[[1]]
[1] "Red"   "Green" "Black"

> print(list[2])
[[1]]
     [,1] [,2] [,3]
[1,]    1    5    9
[2,]    3    7   11

#Q-8
> list <- list(c("Red","Green","Black"), matrix(c(1,3,5,7,9,11), nrow = 2),list("Python", "PHP", "Java"))
> n=length(list)
> list[n] = "New element"
> print(list)
[[1]]
[1] "Red"   "Green" "Black"

[[2]]
     [,1] [,2] [,3]
[1,]    1    5    9
[2,]    3    7   11

[[3]]
[1] "New element"

#Q-9
> x = list(list(0,2), list(3,4), list(5,6))
> e = lapply(x, '[[', 2)
> print(e)
[[1]]
[1] 2

[[2]]
[1] 4

[[3]]
[1] 6
