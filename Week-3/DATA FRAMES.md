#TASK -3(DATA FRAMES)
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



