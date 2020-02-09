# Unit3 Prime numbers #
## Version1 ##
```
n = int(input())

def is_prime_v1(n):
    """Return 'True' if 'n' is a prime number. False otherwise."""
if n == 1:
    return False  #1 is not prime

for d in range(2, n):
    if n % d == 0:
        return False
return True
```
I got some errors for this function which is "'return' is outside of function" and I couldn't figure out how to fix that.
And also I got a question about "return". Does it work same as bool?

