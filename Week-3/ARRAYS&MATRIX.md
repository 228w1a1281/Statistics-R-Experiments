#TASK - 2(ARRAYS  &  MATRIX)
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
