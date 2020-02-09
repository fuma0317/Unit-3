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

## Version2 ##
```
import math

def is_prime_v2(n):
    """Return 'True' if 'n' is a prime number. False otherwise."""
    if n == 1:
        return False # 1 is not prime

    max_divisor = math.floor(math.sqrt(n))
    for d in range(2, 1 + max_divisor):
        if n % d == 0:
            return False
    return True


for n in range(1, 21):
    print(n, is_prime_v2(n))
```
I got some erros about "max_divisor" but I totally understood how this system work.


