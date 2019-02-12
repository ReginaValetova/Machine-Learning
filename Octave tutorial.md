# Octave tutorial

## Basic operations
### Arithmetic operations: 
```octave
5 + 6 % addition
ans = 11

3 - 2 % substraction
ans = 1

4 * 6 % multiplication 
ans = 24

1/2 % division
ans = 0.50000

2^6
ans = 64
```
### Boolean operations:
```octave
1 == 2 & false
ans = 0

1 ~= 2 #not equal
ans = 1

1 && 0 %AND
ans = 0

1 || 0 %OR
ans = 1

xor(1,0)
an = 1
```

### Matrix operations:

 ```octave
A = [1 2; 3 4; 5 6]

A(3,2)
ans = 
    12

A(2,:) % every element along that row
ans = 
    3 11

A(:,2) % every element along that column
ans = 
    10
    11
    12

A([1 3], :)
ans = 
    1   10
    5   12

A(:,2) = [10, 11, 12] % replace operation 
ans = 
    1   10
    3   11
    5   12

A = [A, [100: 101; 102]]; % append another column vector to right
ans =
    1   10  100
    3   11  101
    5   12  102
    
A(:) % put all elements of A into a single vector 
ans = 
    1
    3
    5
    10
    11
    12
    100
    101
    102
```

```octave
B = [11 12 13; 15 16 17; 18 19 20]
C = [A B] % equai to [A, B]
ans = 
    1   2   3   11  12  13
   10  11  12   15  16  17
  100 101 101   18  19  20

D = [A; B]
ans = 

     1     2     3
    10    11    12
   100   101   102
    11    12    13
    15    16    17
    18    19    20
```



```octave
A = [1 2; 3 4; 5 6];
B = [11 12; 13 14; 15 16];
C = [4 5; 6 7];

A * C % matrix multiplication
ans = 
   16   19
   36   43
   56   67

A.*B % multiplicaton by the corresponding elements
ans = 
   11   24
   39   56
   75   96

A.^2
ans = 
    1    4
    9   16
   25   36

1 ./ A
ans =
   1.00000   0.50000
   0.33333   0.25000
   0.20000   0.16667

A'
ans =
   1   3   5
   2   4   6

A < 3
ans =
   1   1
   0   0
   0   0
```


```octave
v = [1 2 3 4]
length(v) 
ans: 
    4

length(A) %(A is a three by two matrix, the longer dimension is of size three)
ans: 
    3 
```

```octave
v = 1:0.5:2
ans =
    1.0000  1.5000  2.0000

v = 1:6
ans = 
    1   2   3   4   5   6
ones = ones(2,3)
ans = 
    1   1   1
    1   1   1

zeros = zeros(1,3)
ans = 
    0   0   0

Identity = eye(3,3) %Identity matrix
ans = 
    1   0   0
    0   1   0
    0   0   1
```

Also Octave is able to built histograms:
```octave
w = -6 + sqrt(34)*randn(1,100000);
hist(w) %histogram
hist(w,30)
```
Output:

<img src="https://i.ibb.co/74WP9WR/2019-02-12-22-32-31.png" alt="drawing" width="550" height="325" />

<img src="https://i.ibb.co/DCjcqmB/2019-02-12-22-31-26.png" alt="drawing" width="550" height="325" />
### Size function
```octave
A = [1 2; 3 4; 5 6]

size(A)
ans = 
    3   2

sz = size(A);

size(sz)
ans = 
    1   2

size(A,1)
ans = 
    3

size(A,2)
ans = 
    2
```

## Moving Data Around
### Terminal Directory Commands

```octave
pwd %print working directory
```
![Alt Text](https://i.ibb.co/QXrkQyp/2019-02-12-23-31-39.png)

```octave
cd "/Users/vinishko/Desktop" %change directory
pwd
```
![Alt Text](https://i.ibb.co/qWQMhwn/2019-02-12-23-33-15.png)

```octave
v = [1; 3; 5; 23; 109; 6];

save hello.txt v -ascii
save hey.txt v
ls
```
![Alt Text](https://i.ibb.co/r6sy7vc/2019-02-13-0-14-29.png)

![Alt Text](https://i.ibb.co/wYLq503/2019-02-13-0-24-58.png)
