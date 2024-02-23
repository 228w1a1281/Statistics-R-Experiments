#Week-1
#Data Frames
#Exercise-1

> studentname=c("valli","vani","vijay","ramu","raju")
> age=c(10,20,39,17,27)
> weight=c(60,50,57,45,70)
> height=c(120,134,156,177,129)
> sex=c("F","F","M","M","M")
> dataframe=data.frame(studentname,age,weight,height,sex)
> dataframe$sex<-ifelse(dataframe$sex=="M","F","M")
> dataframe

#Exercise - 2

> name=c("valli","vani","vijay","ramu","raju")
> Working <- c("Yes","No","No","Yes","Yes")

> df <- data.frame(row.names = name,Working)
> df1<-cbind(dataframe,df)
> df1
> dim(df1)
> str(df1)

#Exercise -3

> class(state.center)
> data.state <- as.data.frame(state.center) 
> data.state 


#Exercise - 4

> a <- (rnorm(10))
> b <- letters[1:10]
> c <- c("yes","no","no","no","no","yes","no","yes","yes","no")
> df2 <- data.frame(a,b,c)
> df2


#Exercise - 5

> matrix.data <- matrix(1:40, nrow = 10, ncol = 4)
> df <- as.data.frame(matrix.data)
> colnames(df1) <- paste("variable_", 1:ncol(df1))
> rownames(df1) <- paste("id_", 1:nrow(df1))
> df1


#Excersice - 6
> class(VADeaths)
[1] "matrix" "array" 
> df3 <- data.frame(VADeaths)
> df3$Total <- rowSums(df3)
> df3 <- df3[,c(5,1,2,3,4)]
> df3


#Exercise - 7
> class(state.x77)
[1] "matrix" "array" 
> df4 <- data.frame(state.x77)
> df4
> nrow(df4[df4$Income < 4300,]) 
> row.names(df4[which.max(df4$Income),])


#Exercise - 8

> df5 <- data.frame(swiss[c(1,2,3,10,11,12,13),c("Examination", "Education", "Infant.Mortality")])
> df5$Infant.Mortality[4] <- NA
> Tot <- colSums(df5, na.rm = TRUE)
> df6 <- rbind(df5,Tot)
> rownames(df6) = c(rownames(df5),"Total")
> df6
> P <- df6$Examination / df6["Total","Examination"]
> df46 <- cbind(df6,P)
> P


#Exercise - 9
> df1 <- data.frame(state.abb, state.area, state.division, state.region, row.names = state.name)
> colnames(df1) <- substr(colnames(df1), 7, 9)
> df1

#Exercise -10

> new.df1 <- cbind(state.x77,df1)
> new.df1$div <- NULL
> new.df1 <- subset(new.df1, ,-c(4, 6, 7, 9, 10))
> new.df1$Illiteracy.Levels <- ifelse(new.df1$Illiteracy >= 0 & new.df1$Illiteracy < 1, "Low",
+                                    ifelse(new.df1$Illiteracy >= 1 & new.df1$Illiteracy < 2, "Some",
+                                           "High"))
> x <- subset(new.df1, reg == "West" & Illiteracy.Levels == "Low")
> 
> row.names(x[which.max(x$Income),]) 
> max(x$Income)




