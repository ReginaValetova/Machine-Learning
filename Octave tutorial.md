# Octave tutorial

## Basic operations
### Arithmetic operations: 
```octave
5 + 6 % addition
3 - 2 % substraction
4 * 6 % multiplication 
1/2 % division
2^6
```
Output:

![Alt Text](https://i.ibb.co/3THbNq3/2019-02-12-17-48-14.png)


### Boolean operations:
```octave
1 == 2 & false
1 ~= 2 #not equal
1 && 0 %AND
1 || 0 %OR
xor(1,0)
```


Output:

![Alt Text](https://i.ibb.co/vqxPVQq/2019-02-12-22-27-08.png)

### Matrix operations:

 ```octave
A = [1 2; 3 4; 5 6]
A(3,2)
A(2,:) % every element along that row
A(:,2) % every element along that column
A([1 3], :)
A(:,2) = [10, 11, 12] % replace operation 
A = [A, [100: 101; 102]]; % append another column vector to right
A(:) % put all elements of A into a single vector 
```
![Alt Text](https://i.ibb.co/ccKHDsL/2019-02-13-1-01-22.png)

```octave
B = [11 12 13; 15 16 17; 18 19 20]
C = [A B] % equai to [A, B]
D = [A; B]
```
![Alt Text](https://i.ibb.co/0VMg7xC/2019-02-13-1-08-02.png)

```octave
size(A) % ans: 3 2
sz = size(A)
size(sz) % ans: 1 2
size(A,1) % ans: 3
size(A,2) % ans: 2
```
Output: 

![Alt Text](https://i.ibb.co/hd79yrz/2019-02-12-23-08-18.png)


```octave
v = [1 2 3 4]
length(v) % ans: 4
length(A) % ans: 3 (A is a three by two matrix, the longer dimension is of size three)
```
Output: 

![Alt Text](https://i.ibb.co/XYpnw23/2019-02-12-23-10-54.png)

```octave
v = 1:0.5:2
v = 1:6

ones = ones(2,3)
zeros = zeros(1,3)
Identity = eye(3,3) %Identity matrix
```

Output: 

![Alt Text](https://i.ibb.co/5YyJh63/2019-02-12-23-11-06.png)

Also Octave is able to built histograms:
```octave
w = -6 + sqrt(34)*randn(1,100000);
hist(w) %histogram
hist(w,30)
```
Output:
![Alt Text](https://i.ibb.co/74WP9WR/2019-02-12-22-32-31.png)
![Alt Text](https://i.ibb.co/DCjcqmB/2019-02-12-22-31-26.png)

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
