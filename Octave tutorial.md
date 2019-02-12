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
 A = [1 2
3 4
5 6]

v = [1 2 3]

v = 1:0.5:2

v = 1:6

ones(2,3)

w = zeros(1,3)

eye(3,3) % identity matrix
```
Output:
![Alt Text](https://i.ibb.co/B4SxwXY/2019-02-12-21-35-41.png)

Also Octave is able to built histograms:
```octave
w = -6 + sqrt(34)*randn(1,100000);
hist(w) %histogram
hist(w,30)
```
Output:
![Alt Text](https://i.ibb.co/74WP9WR/2019-02-12-22-32-31.png)
![Alt Text](https://i.ibb.co/DCjcqmB/2019-02-12-22-31-26.png)