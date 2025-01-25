# Clouds: Numerical Integration 

We saw how to do numerical integration in the class. 

You first task is to create a program that can do numerical integration with the function abs(sin(x)). 

Given an interval lower and upper, your code should break up the interval into $N$ subintervals, compute the area of the rectangle at each subinterval and add them all up. 

For example, if you give as input 0 and 3.14159 (which is approximately $\pi$), you should get $1.99…$ which is close to $2$ ($\int \sin 𝑥 = − \cos 𝑥$, ignoring aspects of continuity, which when evaluated in the range gives you $- \cos \pi + \cos 0 = 2$). 

Your program should loop and repeatedly compute numerical integral for $N = 10, 100, 100, 1000, 10k, 100k, 1M$. You will end up getting 7 values, one for each value of $N$. You will see that as $N$ increases, result converges to 2. 

This will also make the integral computation time consuming which will be useful for load testing later.

## Function

```
func start            
```
> Returns
```powershell
Found Python version 3.12.7 (python3).

Azure Functions Core Tools
Core Tools Version:       4.0.6821 Commit hash: N/A +c09a2033faa7ecf51b3773308283af0ca9a99f83 (64-bit)
Function Runtime Version: 4.1036.1.23224

[2025-01-25T17:09:01.254Z] Worker process started and initialized.

Functions:

	MyPythonFunction:  http://localhost:7071/api/numericalintegralservice

For detailed output, run func with --verbose flag.
[2025-01-25T17:09:06.239Z] Host lock lease acquired by instance ID '00000000000000000000000025882DFC'.
[2025-01-25T17:09:10.443Z] Executing 'Functions.MyPythonFunction' (Reason='This function was programmatically called via the host APIs.', Id=9d829ad1-3501-42ca-a8b9-a7fb3f62dc69)
[2025-01-25T17:09:10.463Z] Python HTTP trigger function processed a request.
[2025-01-25T17:09:10.480Z] Executed 'Functions.MyPythonFunction' (Succeeded, Id=9d829ad1-3501-42ca-a8b9-a7fb3f62dc69, Duration=46ms)
```

- [ ] Testing

http://localhost:7071/api/numericalintegralservice

# References

- [ ] Creating Function

```
func init --python
```
