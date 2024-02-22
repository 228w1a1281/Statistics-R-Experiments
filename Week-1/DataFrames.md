#Week-1
#Data Frames
#Exercise-1

> studentname=c("valli","vani","vijay","ramu","raju")
> age=c(10,20,39,17,27)
> weight=c(60,50,57,45,70)
> height=c(120,134,156,177,129)
> sex=c("F","F","M","M","M")
> dataframe=data.frame(studentname,age,weight,height,sex)
> print(dataframe)
  studentname age weight height sex
1       valli  10     60    120   F
2        vani  20     50    134   F
3       vijay  39     57    156   M
4        ramu  17     45    177   M
5        raju  27     70    129   M
> dataframe$sex<-ifelse(dataframe$sex=="M","F","M")
> dataframe
  studentname age weight height sex
1       valli  10     60    120   M
2        vani  20     50    134   M
3       vijay  39     57    156   F
4        ramu  17     45    177   F
5        raju  27     70    129   F

#Exercise - 2

> name=c("valli","vani","vijay","ramu","raju")
> Working <- c("Yes","No","No","Yes","Yes")

> df <- data.frame(row.names = name,Working)
> df
      Working
valli     Yes
vani       No
vijay      No
ramu      Yes
raju      Yes
> df1<-cbind(dataframe,df)
> df1
      studentname age weight height sex Working
valli       valli  10     60    120   M     Yes
vani         vani  20     50    134   M      No
vijay       vijay  39     57    156   F      No
ramu         ramu  17     45    177   F     Yes
raju         raju  27     70    129   F     Yes
> dim(df1)
[1] 5 6
> str(df1)
'data.frame':	5 obs. of  6 variables:
 $ studentname: chr  "valli" "vani" "vijay" "ramu" ...
 $ age        : num  10 20 39 17 27
 $ weight     : num  60 50 57 45 70
 $ height     : num  120 134 156 177 129
 $ sex        : chr  "M" "M" "F" "F" ...
 $ Working    : chr  "Yes" "No" "No" "Yes" ...
 
#Exercise -3

> class(state.center)
[1] "list"
> data.state <- as.data.frame(state.center) 
> data.state 
           x       y
1   -86.7509 32.5901
2  -127.2500 49.2500
3  -111.6250 34.2192
4   -92.2992 34.7336
5  -119.7730 36.5341
6  -105.5130 38.6777
7   -72.3573 41.5928
8   -74.9841 38.6777
9   -81.6850 27.8744
10  -83.3736 32.3329
11 -126.2500 31.7500
12 -113.9300 43.5648
13  -89.3776 40.0495
14  -86.0808 40.0495
15  -93.3714 41.9358
16  -98.1156 38.4204
17  -84.7674 37.3915
18  -92.2724 30.6181
19  -68.9801 45.6226
20  -76.6459 39.2778
21  -71.5800 42.3645
22  -84.6870 43.1361
23  -94.6043 46.3943
24  -89.8065 32.6758
25  -92.5137 38.3347
26 -109.3200 46.8230
27  -99.5898 41.3356
28 -116.8510 39.1063
29  -71.3924 43.3934
30  -74.2336 39.9637
31 -105.9420 34.4764
32  -75.1449 43.1361
33  -78.4686 35.4195
34 -100.0990 47.2517
35  -82.5963 40.2210
36  -97.1239 35.5053
37 -120.0680 43.9078
38  -77.4500 40.9069
39  -71.1244 41.5928
40  -80.5056 33.6190
41  -99.7238 44.3365
42  -86.4560 35.6767
43  -98.7857 31.3897
44 -111.3300 39.1063
45  -72.5450 44.2508
46  -78.2005 37.5630
47 -119.7460 47.4231
48  -80.6665 38.4204
49  -89.9941 44.5937
50 -107.2560 43.0504

#Exercise - 4

> a <- (rnorm(10))
> b <- letters[1:10]
> c <- c("yes","no","no","no","no","yes","no","yes","yes","no")
> df2 <- data.frame(a,b,c)
> df2
            a b   c
1  -0.5766386 a yes
2  -2.2381393 b  no
3  -0.2057544 c  no
4  -2.7527639 d  no
5   0.4342399 e  no
6  -0.7560620 f yes
7  -1.5512777 g  no
8   0.2895139 h yes
9  -0.6270879 i yes
10  0.7188328 j  no

#Exercise - 5

> matrix.data <- matrix(1:40, nrow = 10, ncol = 4)
> df <- as.data.frame(matrix.data)
> 
> colnames(df1) <- paste("variable_", 1:ncol(df1))
> rownames(df1) <- paste("id_", 1:nrow(df1))
> df1
      variable_ 1 variable_ 2 variable_ 3 variable_ 4 variable_ 5 variable_ 6
id_ 1       valli          10          60         120           M         Yes
id_ 2        vani          20          50         134           M          No
id_ 3       vijay          39          57         156           F          No
id_ 4        ramu          17          45         177           F         Yes
id_ 5        raju          27          70         129           F         Yes

#Excersice - 6
> class(VADeaths)
[1] "matrix" "array" 
> df3 <- data.frame(VADeaths)
> df3$Total <- rowSums(df3)
> df3 <- df3[,c(5,1,2,3,4)]
> df3
      Total Rural.Male Rural.Female Urban.Male Urban.Female
50-54  44.2       11.7          8.7       15.4          8.4
55-59  67.7       18.1         11.7       24.3         13.6
60-64 103.5       26.9         20.3       37.0         19.3
65-69 161.6       41.0         30.9       54.6         35.1
70-74 241.4       66.0         54.3       71.1         50.0

#Exercise - 7
> class(state.x77)
[1] "matrix" "array" 
> df4 <- data.frame(state.x77)
> df4
               Population Income Illiteracy Life.Exp Murder HS.Grad Frost   Area
Alabama              3615   3624        2.1    69.05   15.1    41.3    20  50708
Alaska                365   6315        1.5    69.31   11.3    66.7   152 566432
Arizona              2212   4530        1.8    70.55    7.8    58.1    15 113417
Arkansas             2110   3378        1.9    70.66   10.1    39.9    65  51945
California          21198   5114        1.1    71.71   10.3    62.6    20 156361
Colorado             2541   4884        0.7    72.06    6.8    63.9   166 103766
Connecticut          3100   5348        1.1    72.48    3.1    56.0   139   4862
Delaware              579   4809        0.9    70.06    6.2    54.6   103   1982
Florida              8277   4815        1.3    70.66   10.7    52.6    11  54090
Georgia              4931   4091        2.0    68.54   13.9    40.6    60  58073
Hawaii                868   4963        1.9    73.60    6.2    61.9     0   6425
Idaho                 813   4119        0.6    71.87    5.3    59.5   126  82677
Illinois            11197   5107        0.9    70.14   10.3    52.6   127  55748
Indiana              5313   4458        0.7    70.88    7.1    52.9   122  36097
Iowa                 2861   4628        0.5    72.56    2.3    59.0   140  55941
Kansas               2280   4669        0.6    72.58    4.5    59.9   114  81787
Kentucky             3387   3712        1.6    70.10   10.6    38.5    95  39650
Louisiana            3806   3545        2.8    68.76   13.2    42.2    12  44930
Maine                1058   3694        0.7    70.39    2.7    54.7   161  30920
Maryland             4122   5299        0.9    70.22    8.5    52.3   101   9891
Massachusetts        5814   4755        1.1    71.83    3.3    58.5   103   7826
Michigan             9111   4751        0.9    70.63   11.1    52.8   125  56817
Minnesota            3921   4675        0.6    72.96    2.3    57.6   160  79289
Mississippi          2341   3098        2.4    68.09   12.5    41.0    50  47296
Missouri             4767   4254        0.8    70.69    9.3    48.8   108  68995
Montana               746   4347        0.6    70.56    5.0    59.2   155 145587
Nebraska             1544   4508        0.6    72.60    2.9    59.3   139  76483
Nevada                590   5149        0.5    69.03   11.5    65.2   188 109889
New Hampshire         812   4281        0.7    71.23    3.3    57.6   174   9027
New Jersey           7333   5237        1.1    70.93    5.2    52.5   115   7521
New Mexico           1144   3601        2.2    70.32    9.7    55.2   120 121412
New York            18076   4903        1.4    70.55   10.9    52.7    82  47831
North Carolina       5441   3875        1.8    69.21   11.1    38.5    80  48798
North Dakota          637   5087        0.8    72.78    1.4    50.3   186  69273
Ohio                10735   4561        0.8    70.82    7.4    53.2   124  40975
Oklahoma             2715   3983        1.1    71.42    6.4    51.6    82  68782
Oregon               2284   4660        0.6    72.13    4.2    60.0    44  96184
Pennsylvania        11860   4449        1.0    70.43    6.1    50.2   126  44966
Rhode Island          931   4558        1.3    71.90    2.4    46.4   127   1049
South Carolina       2816   3635        2.3    67.96   11.6    37.8    65  30225
South Dakota          681   4167        0.5    72.08    1.7    53.3   172  75955
Tennessee            4173   3821        1.7    70.11   11.0    41.8    70  41328
Texas               12237   4188        2.2    70.90   12.2    47.4    35 262134
Utah                 1203   4022        0.6    72.90    4.5    67.3   137  82096
Vermont               472   3907        0.6    71.64    5.5    57.1   168   9267
Virginia             4981   4701        1.4    70.08    9.5    47.8    85  39780
Washington           3559   4864        0.6    71.72    4.3    63.5    32  66570
West Virginia        1799   3617        1.4    69.48    6.7    41.6   100  24070
Wisconsin            4589   4468        0.7    72.48    3.0    54.5   149  54464
Wyoming               376   4566        0.6    70.29    6.9    62.9   173  97203

> nrow(df4[df4$Income < 4300,]) 
[1] 20

> row.names(df4[which.max(df4$Income),])
[1] "Alaska"

#Exercise - 8

> df5 <- data.frame(swiss[c(1,2,3,10,11,12,13),c("Examination", "Education", "Infant.Mortality")])
> df5$Infant.Mortality[4] <- NA
> Tot <- colSums(df5, na.rm = TRUE)
> df6 <- rbind(df5,Tot)
> rownames(df6) = c(rownames(df5),"Total")
> df6
             Examination Education Infant.Mortality
Courtelary            15        12             22.2
Delemont               6         9             22.2
Franches-Mnt           5         5             20.2
Sarine                16        13               NA
Veveyse               14         6             24.5
Aigle                 21        12             16.5
Aubonne               14         7             19.1
Total                 91        64            124.7
> P <- df6$Examination / df6["Total","Examination"]
>
> P
[1] 0.16483516 0.06593407 0.05494505 0.17582418 0.15384615 0.23076923 0.15384615
[8] 1.00000000
> df46 <- cbind(df6,P)
> P
[1] 0.16483516 0.06593407 0.05494505 0.17582418 0.15384615 0.23076923 0.15384615
[8] 1.00000000

#Exercise - 9
> df1 <- data.frame(state.abb, state.area, state.division, state.region, row.names = state.name)
> colnames(df1) <- substr(colnames(df1), 7, 9)
> df1
               abb    are                div           reg
Alabama         AL  51609 East South Central         South
Alaska          AK 589757            Pacific          West
Arizona         AZ 113909           Mountain          West
Arkansas        AR  53104 West South Central         South
California      CA 158693            Pacific          West
Colorado        CO 104247           Mountain          West
Connecticut     CT   5009        New England     Northeast
Delaware        DE   2057     South Atlantic         South
Florida         FL  58560     South Atlantic         South
Georgia         GA  58876     South Atlantic         South
Hawaii          HI   6450            Pacific          West
Idaho           ID  83557           Mountain          West
Illinois        IL  56400 East North Central North Central
Indiana         IN  36291 East North Central North Central
Iowa            IA  56290 West North Central North Central
Kansas          KS  82264 West North Central North Central
Kentucky        KY  40395 East South Central         South
Louisiana       LA  48523 West South Central         South
Maine           ME  33215        New England     Northeast
Maryland        MD  10577     South Atlantic         South
Massachusetts   MA   8257        New England     Northeast
Michigan        MI  58216 East North Central North Central
Minnesota       MN  84068 West North Central North Central
Mississippi     MS  47716 East South Central         South
Missouri        MO  69686 West North Central North Central
Montana         MT 147138           Mountain          West
Nebraska        NE  77227 West North Central North Central
Nevada          NV 110540           Mountain          West
New Hampshire   NH   9304        New England     Northeast
New Jersey      NJ   7836    Middle Atlantic     Northeast
New Mexico      NM 121666           Mountain          West
New York        NY  49576    Middle Atlantic     Northeast
North Carolina  NC  52586     South Atlantic         South
North Dakota    ND  70665 West North Central North Central
Ohio            OH  41222 East North Central North Central
Oklahoma        OK  69919 West South Central         South
Oregon          OR  96981            Pacific          West
Pennsylvania    PA  45333    Middle Atlantic     Northeast
Rhode Island    RI   1214        New England     Northeast
South Carolina  SC  31055     South Atlantic         South
South Dakota    SD  77047 West North Central North Central
Tennessee       TN  42244 East South Central         South
Texas           TX 267339 West South Central         South
Utah            UT  84916           Mountain          West
Vermont         VT   9609        New England     Northeast
Virginia        VA  40815     South Atlantic         South
Washington      WA  68192            Pacific          West
West Virginia   WV  24181     South Atlantic         South
Wisconsin       WI  56154 East North Central North Central
Wyoming         WY  97914           Mountain          West

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
[1] "Nevada"
> max(x$Income)
[1] 5149



