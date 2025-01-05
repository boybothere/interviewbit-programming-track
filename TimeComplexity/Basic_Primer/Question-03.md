What is the time complexity of the following code :

    int a = 0;
    for (i = 0; i < N; i++) {        //Loop1
        for (j = N; j > i; j--) {    //Loop2
            a = a + i + j;
        }
    }

Solution: Here Loop1 and Loop2 are nested now lets analyse this by considering N as 5

1st iteration: i = 0 also j = 5 and runs till j > 0 hence inner loop runs " 5 times "
2nd iteration: i = 1 also j = 4 and runs till j > 1 hence inner loop runs " 4 times "
3rd iteration: i = 2 also j = 3 and runs till j > 2 hence inner loop runs " 3 times "
4th iteration: i = 3 also j = 2 and runs till j > 3 hence inner loop runs " 2 times "
5th iteration: i = 4 also j = 1 and runs till j > 5 hence inner loop runs " 1 times "

Therefore we 5 + 4 + 3 + ...+ 1 = N*(N+1)/2 [Sum of series tending to 1 with N numbers]
This simplifies to to N^2/2 + N/2
In Big-O analysis, we ignore constants and lower-order terms(the N term). Hence, the time complexity simplifies to O(N^2)
