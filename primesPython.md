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

## Version3 ##
```
import math

def is_prime_v3(n):
    """Return 'True' if 'n' is a prime number. False otherwise."""
    if n == 1:
        return False # 1 is not prime

    #if it's even and not 2, then it's not prime
    if n == 2:
        return True
    if n > 2 and n % 2 == 0:
        return False

    max_divisor = math.floor(math.sqrt(n))
    for d in range(3, 1 + max_divisor, 2):
        if n % d == 0:
            return False
    return True


for n in range(1, 21):
    print(n, is_prime_v3(n))
```
I got some errors and code does work until 2..
But I understood how the code work.


