# Fibonacci
Fibonacci is a sequence of numbers staring from 0 until an infinite number of additions of the N-1 and N-2. With N being the current value. For example we can look at the sequence which is 0 1 1 2 3 5 8 13 21 34 55 and so on. So the formula to actually get each value within the Fibonacci sequence N = Current value within the sequence being N - 1 + N -2 for example we could look at value 5 which is 3 so how to get 3 would be N - 1 which is 2 and N - 2 which is 1 so 2 + 1 = 3. The only rule within the sequence is the first N value has to be 0 and the second N value has to be 1.
# Fibonacci Iterative
```c
int fibonacciIterative(int N){
    int num1=0;
    int num2=1;
    int output;

    if (N==0) {
        return num1;
    } else if (N==1){
        return num2;
    } else {
        for (int i = 2; i<= N; i++){ 
            output = num1+num2;
            num1 = num2;
            num2 = output;
        }
        return output;
    }
}
```
# Fibonacci Recursive
```c
int fibonacciRecursive (int N){
    if (N==0){
        return 0;
    } else if (N==1){
        return 1;
    } else {
        return fibonacciRecursive(N - 1) + fibonacciRecursive(N-2);
    }
}
```
# OutPut
![same](image/same.png)
# Time Complexity Output
Test were ran between the two methods of running the fibonacci sequence within both recursive form and iterative form to see the time complexity of both methods. this was done using the code provided by Sir Ardimas which resulted in the below times.

![time1](image/time_iterative.png)
![time2](image/time_recursive.png)

through the test we can see that recursive's time is better then iterative which mean it has a faster time to complete the task at hand because within iterative format it takes time to check for each value while within recursive format it loops within it self by calling its own fucntion creating a loop within a loop that only does addition creating a faster time.

# Space Complexity Output
Test were ran again between the two methods of running a fibonacci sequence within both recursive form and iterative form to see the space complexity of both methods. this was done the code provided by Sir Ardimas which resulted in the below space usage which was taken from the task manager.

![space](image/space.png)

through the test we can see that recursive's space complexity is higher then iterative this is due to the fact that recursice does more commands in each call of the function per N -1 and N -2. while looping divides it equally for each instead.
