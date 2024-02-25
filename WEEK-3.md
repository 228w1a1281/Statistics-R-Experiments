#WEEK-3
#TASK-1
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

#TASK - 2
#Q-1
> l = list()
> n=length(list)
> for (i in 1:n) l[[i]] <- c(i, 1:n-1)
> print(l)
[[1]]
[1] 1 0 1 2

[[2]]
[1] 2 0 1 2

[[3]]
[1] 3 0 1 2

> result = do.call(rbind, l)
> print(result)
     [,1] [,2] [,3] [,4]
[1,]    1    0    1    2
[2,]    2    0    1    2
[3,]    3    0    1    2

#Q-2
> row_names = c("row1", "row2", "row3", "row4")
> col_names = c("col1", "col2", "col3", "col4")
> M = matrix(c(1:16), nrow = 4, byrow = TRUE, dimnames = list(row_names, col_names))
> print(M)
     col1 col2 col3 col4
row1    1    2    3    4
row2    5    6    7    8
row3    9   10   11   12
row4   13   14   15   16
> result = M[M[,3] > 7,]
> print(result)
     col1 col2 col3 col4
row3    9   10   11   12
row4   13   14   15   16

#Q-3
> m=matrix(1:12,3,4)
> a = as.vector(m)
> print(m)
     [,1] [,2] [,3] [,4]
[1,]    1    4    7   10
[2,]    2    5    8   11
[3,]    3    6    9   12
> print(a)
 [1]  1  2  3  4  5  6  7  8  9 10 11 12
 
#Q-4
> m = matrix(c(1:16), nrow = 4, byrow = TRUE)
> print(m)
     [,1] [,2] [,3] [,4]
[1,]    1    2    3    4
[2,]    5    6    7    8
[3,]    9   10   11   12
[4,]   13   14   15   16
> result = which(m == max(m), arr.ind=TRUE)
> print(result)
     row col
[1,]   4   4
> result = which(m == min(m), arr.ind=TRUE)
> print(result)
     row col
[1,]   1   1

#Q-5
> v1 =  c(1,3,4,5)
> v2 =  c(10,11,12,13,14,15)
> result = array(c(v1,v2),dim = c(3,3,2))
> print(result)
, , 1

     [,1] [,2] [,3]
[1,]    1    5   12
[2,]    3   10   13
[3,]    4   11   14

, , 2

     [,1] [,2] [,3]
[1,]   15    4   11
[2,]    1    5   12
[3,]    3   10   13


#Q-6
> v =  sample(1:5,24,replace = TRUE)
> dim(v) = c(3,2,4)
> print(v)
, , 1

     [,1] [,2]
[1,]    4    5
[2,]    5    5
[3,]    5    1

, , 2

     [,1] [,2]
[1,]    3    4
[2,]    4    3
[3,]    1    2

, , 3

     [,1] [,2]
[1,]    4    3
[2,]    2    3
[3,]    5    3

, , 4

     [,1] [,2]
[1,]    3    3
[2,]    1    3
[3,]    5    1

#Q-7
> v1 =  c(1,3,4,5)
> v2 =  c(10,11,12,13,14,15)
> result = array(c(v1,v2),dim = c(3,3,2))
> print(result)
, , 1

     [,1] [,2] [,3]
[1,]    1    5   12
[2,]    3   10   13
[3,]    4   11   14

, , 2

     [,1] [,2] [,3]
[1,]   15    4   11
[2,]    1    5   12
[3,]    3   10   13

> print(result[2,,2])
[1]  1  5 12
> print(result[3,3,1])
[1] 14

#Q-8
> num1 = rbind(rep("A",3), rep("B",3), rep("C",3))
> num2 = rbind(rep("P",3), rep("Q",3), rep("R",3))
> num3 = rbind(rep("X",3), rep("Y",3), rep("Z",3))
> a = matrix(t(cbind(num1,num2,num3)),ncol=3, byrow=T)
> print(a)
      [,1] [,2] [,3]
 [1,] "A"  "A"  "A" 
 [2,] "P"  "P"  "P" 
 [3,] "X"  "X"  "X" 
 [4,] "B"  "B"  "B" 
 [5,] "Q"  "Q"  "Q" 
 [6,] "Y"  "Y"  "Y" 
 [7,] "C"  "C"  "C" 
 [8,] "R"  "R"  "R" 
 [9,] "Z"  "Z"  "Z" 
 
#TASK -3
#Q-1
> name = c('SITA', 'RAMU', 'VARMA', 'SAM', 'VIJAY', 'RAVI', 'RAJU', 'RANI', 'VANI', 'VALLI')
> score = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19)
> a = c(1, 3, 2, 3, 2, 3, 1, 1, 2, 1)
> q = c('yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes')
> df = data.frame(name, score, a, q)
> df
    name score a   q
1   SITA  12.5 1 yes
2   RAMU   9.0 3  no
3  VARMA  16.5 2 yes
4    SAM  12.0 3  no
5  VIJAY   9.0 2  no
6   RAVI  20.0 3 yes
7   RAJU  14.5 1 yes
8   RANI  13.5 1  no
9   VANI   8.0 2  no
10 VALLI  19.0 1 yes

#Q-2
> exam_data = data.frame(
+ name = c('SITA', 'RAMU', 'VARMA', 'SAM', 'VIJAY', 'RAVI', 'RAJU', 'RANI', 'VANI', 'VALLI'),
+ score = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19),
+ a = c(1, 3, 2, 3, 2, 3, 1, 1, 2, 1),
+ q = c('yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes'))
> print(exam_data)
    name score a   q
1   SITA  12.5 1 yes
2   RAMU   9.0 3  no
3  VARMA  16.5 2 yes
4    SAM  12.0 3  no
5  VIJAY   9.0 2  no
6   RAVI  20.0 3 yes
7   RAJU  14.5 1 yes
8   RANI  13.5 1  no
9   VANI   8.0 2  no
10 VALLI  19.0 1 yes
> print(summary(exam_data))
     name               score             a             q            
 Length:10          Min.   : 8.00   Min.   :1.00   Length:10         
 Class :character   1st Qu.: 9.75   1st Qu.:1.00   Class :character  
 Mode  :character   Median :13.00   Median :2.00   Mode  :character  
                    Mean   :13.40   Mean   :1.90                     
                    3rd Qu.:16.00   3rd Qu.:2.75                     
                    Max.   :20.00   Max.   :3.00 
                    
#Q-3
> exam_data = data.frame(
+ name = c('SITA', 'RAMU', 'VARMA', 'SAM', 'VIJAY', 'RAVI', 'RAJU', 'RANI', 'VANI', 'VALLI'),
+ score = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19),
+ a = c(1, 3, 2, 3, 2, 3, 1, 1, 2, 1),
+ q = c('yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes'))
> result <- data.frame(exam_data$name,exam_data$score)
> print(result)


# Q-4
> exam_data = data.frame(
+ name = c('SITA', 'RAMU', 'VARMA', 'SAM', 'VIJAY', 'RAVI', 'RAJU', 'RANI', 'VANI', 'VALLI'),
+ score = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19),
+ a = c(1, 3, 2, 3, 2, 3, 1, 1, 2, 1),
+ q = c('yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes'))
> result =  exam_data[c(3,5),c(1,3)]
> print(result)


#Q-5
> exam_data = data.frame(
+ name = c('SITA', 'RAMU', 'VARMA', 'SAM', 'VIJAY', 'RAVI', 'RAJU', 'RANI', 'VANI', 'VALLI'),
+ score = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19),
+ a = c(1, 3, 2, 3, 2, 3, 1, 1, 2, 1),
+ q = c('yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes'))
> new_row= data.frame(
+ name = c('Robert', 'Sophia'),
+ score = c(10.5, 9),
+ a = c(1, 3),
+ q = c('yes', 'no'))
> rows_ex =  rbind(exam_data, new_row)
> print(rows_ex)
> exam_data$city= c("vijayawda","vijayawda","vijayawda","vijayawda","vijayawda","vijayawda","vijayawda","vijayawda","vijayawda","vijayawda")
> print(exam_data)



