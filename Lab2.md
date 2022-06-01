В лабораторній роботі необхідно виконати наступні дії:
1. Створить векторv із 100 елементів командою v<-rnorm(100).Для цього вектору виведіть: 10-й елемент; елементи з 10-го по 20-й включно; 10
елементів починаючи з 20-го; елементи більше 0.
```R

> v<-rnorm(100)
> v
  [1] -2.233432527 -0.005334088  2.950140828  0.390871650  0.678041364
  [6] -0.749698785  0.627779172 -1.120492990  0.693673885  0.403545108
 [11]  1.298666822 -1.178727814  0.533706931 -0.469227935  0.098372816
 [16] -0.012802268  0.159064474  0.967774159  0.069751341  0.822377470
 [21]  0.148841463 -1.102101023 -0.240821068 -1.025273613 -0.749311978
 [26] -0.734262041 -0.143987239 -0.392178323  0.730389804 -3.151413455
 [31] -1.752164280 -0.009951662  0.596887573  1.145428363 -1.014477563
 [36]  0.271885643  0.125540436 -1.237898710 -1.832456356 -0.261163588
 [41] -0.300415488  0.072227867 -0.093927897 -0.652560251  0.774436412
 [46]  0.467780451  0.800837185 -0.344456075 -0.887546613  0.208625544
 [51] -0.684815063  0.317129841 -0.527501899 -0.504930229  0.043408695
 [56] -1.429737669  1.045519596  0.484943146  1.597873114  0.473441125
 [61]  0.603489447 -0.181874638  0.530981673  0.908691246  1.622957544
 [66]  0.137372156  2.292555573  0.961849142 -0.939268947 -0.093590561
 [71]  0.744799396 -0.815788630  2.460243408  0.607204807 -1.274634858
 [76]  1.939283005 -0.504810280 -2.182234395 -0.083010377 -1.526277717
 [81] -0.283130080 -0.174794693  0.320364626 -1.790411094  0.297298658
 [86] -0.735103679 -0.015145892 -1.188269027 -0.646548781 -1.051949668
 [91] -1.418837970 -0.176571384 -0.074770976 -0.895822081  0.255424967
 [96]  0.598912971 -0.400392785 -0.928956148 -0.350117576 -0.541337970

> #10th element
> v[10]
[1] 0.4035451

> #from 10 to 20
> v[10:20]
 [1]  0.40354511  1.29866682 -1.17872781  0.53370693 -0.46922793  0.09837282
 [7] -0.01280227  0.15906447  0.96777416  0.06975134  0.82237747

> #10 elements from 20
> v[20:29]
 [1]  0.8223775  0.1488415 -1.1021010
 [4] -0.2408211 -1.0252736 -0.7493120
 [7] -0.7342620 -0.1439872 -0.3921783
[10]  0.7303898

> #greater than 0
> v[v>0]
  [1] 2.95014083 0.39087165 0.67804136
 [4] 0.62777917 0.69367389 0.40354511
 [7] 1.29866682 0.53370693 0.09837282
[10] 0.15906447 0.96777416 0.06975134
[13] 0.82237747 0.14884146 0.73038980
[16] 0.59688757 1.14542836 0.27188564
[19] 0.12554044 0.07222787 0.77443641
[22] 0.46778045 0.80083718 0.20862554
[25] 0.31712984 0.04340870 1.04551960
[28] 0.48494315 1.59787311 0.47344112
[31] 0.60348945 0.53098167 0.90869125
[34] 1.62295754 0.13737216 2.29255557
[37] 0.96184914 0.74479940 2.46024341
[40] 0.60720481 1.93928300 0.32036463
[43] 0.29729866 0.25542497 0.59891297
```


2. Створити фрейм (data frame) y командою y <- data.frame(a = rnorm(100), b = 1:100, cc = sample(letters, 100, replace = TRUE)). Для цього data frame виведіть: останні 10 строк; строки з 10 по 20 включно; 10-й елемент стовпця b; повністю стовпець cc, при цьому використайте ім’я стовпця.
```R

> y<-data.frame(a=rnorm(100),b=1:100,cc=sample(letters,100,replace=TRUE))
> y
     a   b cc
1    0.27032341   1  c
2    0.89309232   2  d
3    0.06931939   3  t
4   -0.01178598   4  g
5    1.49983864   5  s
6   -0.72066892   6  o
7   -0.25647084   7  k
8    0.20770413   8  d
9   -1.12980233   9  e
10   0.50493481  10  l
11   0.78216120  11  p
12  -0.43320613  12  g
13  -1.58578944  13  i
14  -0.27780606  14  o
15   0.27605844  15  l
16  -2.10292988  16  m
17   0.11446693  17  l
18  -0.64023864  18  e
19   0.19557252  19  f
20   0.44879606  20  n
21  -0.43858841  21  v
22  -1.42627971  22  v
23  -0.98283522  23  s
24  -0.67434788  24  r
25  -0.83041198  25  r
26   0.35109830  26  v
27  -0.18139609  27  i
28  -0.65742527  28  j
29   1.35946493  29  p
30  -0.49492867  30  o
31   0.85616274  31  h
32  -1.08279682  32  a
33  -1.05924123  33  u
34   0.97088699  34  q
35   1.34832903  35  l
36   0.31393714  36  m
37   0.19172736  37  l
38   0.76687140  38  a
39   2.28985572  39  q
40  -2.97190736  40  n
41  -1.19783093  41  g
42   0.01469301  42  l
43  -0.07310162  43  m
44   1.06561951  44  v
45   0.73994570  45  b
46  -0.39467060  46  i
47  -1.36352732  47  r
48   2.82139225  48  s
49  -1.93507584  49  s
50  -0.75306834  50  z
51  -0.78334269  51  x
52  -0.66609367  52  v
53   2.27102986  53  z
54   0.43112342  54  e
55   0.13993401  55  o
56  -1.69866967  56  f
57  -0.17331807  57  y
58   0.44380226  58  j
59   1.49151621  59  a
60   1.80044588  60  y
61  -0.68167557  61  h
62  -0.73424711  62  m
63   0.64991509  63  c
64   0.51086549  64  b
65   0.08864111  65  x
66   0.36316867  66  n
67  -1.20790362  67  t
68  -0.13435011  68  u
69  -0.43316352  69  f
70   0.38091966  70  f
71   0.34711118  71  x
72  -0.02874322  72  m
73  -1.21031301  73  d
74  -0.68872126  74  l
75   0.71939367  75  i
76   0.77740424  76  u
77  -0.26062406  77  d
78   0.58951122  78  o
79   0.22043707  79  w
80  -0.37797493  80  w
81   0.80253739  81  z
82   0.22407923  82  v
83   0.59549035  83  g
84   0.62106338  84  t
85   0.21769621  85  k
86  -0.23066638  86  i
87   0.27813848  87  l
88  -0.15333810  88  g
89  -0.99046855  89  z
90   2.09075192  90  a
91   1.05943040  91  j
92   0.42584783  92  p
93   0.58534405  93  f
94   0.17916755  94  k
95   0.76353921  95  h
96   0.78253199  96  z
97   0.41818234  97  h
98  -0.97366724  98  q
99  -1.98539393  99  x
100  0.06942780 100  c

> # last 10 records
> y[91:100, ]
            a   b cc
91   1.0594304  91  j
92   0.4258478  92  p
93   0.5853441  93  f
94   0.1791676  94  k
95   0.7635392  95  h
96   0.7825320  96  z
97   0.4181823  97  h
98  -0.9736672  98  q
99  -1.9853939  99  x
100  0.0694278 100  c

> #rows from 10 to 20
> y[10:20, ]
             a  b cc
10  0.5049348 10  l
11  0.7821612 11  p
12 -0.4332061 12  g
13 -1.5857894 13  i
14 -0.2778061 14  o
15  0.2760584 15  l
16 -2.1029299 16  m
17  0.1144669 17  l
18 -0.6402386 18  e
19  0.1955725 19  f
20  0.4487961 20  n

> #10th row from b column
> y[10,'b']
[1] 10

> #cc column with using column name
> y[['cc']]
    [1] "c" "d" "t" "g" "s" "o" "k" "d" "e" "l" "p" "g" "i" "o" "l" "m" "l"
 [18] "e" "f" "n" "v" "v" "s" "r" "r" "v" "i" "j" "p" "o" "h" "a" "u" "q"
 [35] "l" "m" "l" "a" "q" "n" "g" "l" "m" "v" "b" "i" "r" "s" "s" "z" "x"
 [52] "v" "z" "e" "o" "f" "y" "j" "a" "y" "h" "m" "c" "b" "x" "n" "t" "u"
 [69] "f" "f" "x" "m" "d" "l" "i" "u" "d" "o" "w" "w" "z" "v" "g" "t" "k"
 [86] "i" "l" "g" "z" "a" "j" "p" "f" "k" "h" "z" "h" "q" "x" "c"
 ```
 
 3. Створити вектор z з елементами 1,2,3,NA,4,NA,5,NA. Для цього вектору: виведіть всі елементи, які не NA; підрахуйте середнє значення всіх елементів цього вектору без NA значень та з NA значеннями.
```R
> z<-c(1, 2, 3, NA, 4, NA, 5, NA)
> z
[1]  1  2  3 NA  4 NA  5 NA

> #values not equal NA
> z_na<-is.na(z)
> z_na
[1] FALSE FALSE FALSE  TRUE FALSE  TRUE FALSE  TRUE
> z[!z_na]
[1] 1 2 3 4 5

> #mean of vector without NA
> mean(z[!z_na])
[1] 3

> #mean of vector with NA
> mean(z)
[1] NA
```