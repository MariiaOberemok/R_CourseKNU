В лабораторній роботі необхідно виконати наступні дії:


1. Створити змінні базових (atomic) типів. Базові типи: character, numeric,
integer, complex, logical.
```R 
x1<-'Character' 
x2<-2022      
x3<-2L     
x4<- 2 + 2i  
x5<- TRUE   

x1
[1] "Character"
x2
[1] 2022
x3
[1] 2
x4
[1] 2+2i
x5
[1] TRUE
```


2. Створити вектори, які: містить послідовність з 5 до 75; містить числа 3.14,
  2.71, 0, 13; 100 значень TRUE.
  
  ```R 
vector1 <- 5:75
vector2 <- c(3.14,2.71,0,13)
vector3 <- rep(TRUE,100)

vector1
 [1]  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47
[44] 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75
vector2
[1]  3.14  2.71  0.00 13.00
vector3
  [1] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [26] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [51] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
 [76] TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE TRUE
```


3. Створити наступну матрицю за допомогою matrix, та за допомогою cbind або rbind

```R
0.5 1.3 3.5 
3.9 131 2.8 
0   2.2 4.6 
2   7   5.1

matrix1<- matrix (c(0.5, 1.3, 3.5, 3.9, 131, 2.8, 0, 2.2, 4.6, 2, 7, 5.1), nrow=4, ncol=3, byrow=TRUE)
#or
matrix11<-matrix(c(0.5,3.9,0,2,1.3,131,2.2,7,3.5,2.8,4.6,5.1),ncol=3,nrow=4)

matrix2<-cbind(c(0.5,3.9,0,2),c(1.3,131,2.2,7),c(3.5,2.8,4.6,5.1))
matrix3<-rbind(c(0.5,1.3,3.5),c(3.9,131,2.8),c(0,2.2,4.6),c(2,7,5.1))

matrix1
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
matrix11
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
matrix2
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
matrix3
     [,1]  [,2] [,3]
[1,]  0.5   1.3  3.5
[2,]  3.9 131.0  2.8
[3,]  0.0   2.2  4.6
[4,]  2.0   7.0  5.1
```


4. Створити довільний список(list),в який включити всі базові типи.
```R
> x<- list('ab',10,123L,TRUE,2+2i)
> print(x)
```
```R
[[1]]
[1] "ab"

[[2]]
[1] 10

[[3]]
[1] 123

[[4]]
[1] TRUE

[[5]]
[1] 2+2i
```


5. Створити фактор з трьома рівнями«baby»,«child»,«adult».
```R
x<-factor(c("baby",'child','baby','baby', 'adult', 'child','child', 'adult','baby','adult'))
print(x)
table(x)
```
```R
 [1] baby  child baby  baby  adult child child adult baby  adult
Levels: adult baby child
x
adult  baby child 
    3     4     3 
```


6. Знайти індекс першого значення NA в векторі 1,2,3,4,NA,6,7,NA,9,NA, 11. Знайти кількість значень NA.
```R
x<-c(1,2,3,4,NA,6,7,NA,9,NA,11)
match(NA, x)
```
```R
[1] 5
```
```R
length(which(is.na(x)))
```
```R
[1] 3
```

7. Створитидовільнийdataframeтавивестивконсоль.
```R
data_frame<-data.frame(order=c(101:105),costs=c(1200,700,350,5100,1000), manager=c(3,4,4,2,8))

data_frame
  order  costs  manager
1  101   1200    3
2  102   700     4
3  103   350     4
4  104   5100    2
5  105   1000    8  
```


8. Змінити імена стовпців цього data frame.
```{R}
colnames(data_frame) <- c("number", "amount", "executive")

data_frame
 number  amount  executive
1  101   1200    3
2  102   700     4
3  103   350     4
4  104   5100    2
5  105   1000    8  
```
