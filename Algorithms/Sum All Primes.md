## Sum All Primes

### Description
Sum all the prime numbers up to and including the provided number.

A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two.

The provided number may not be a prime.

### Code

```javascript


function prime(n) {
  if (n < 2) return false;
  var m = Math.floor(Math.sqrt(n));
  for (var i = 2; i <= m; i++)
    {
      if (n % i===0) return false;
    }
  return true;
}

function sumPrimes(num) {
  var sum = 0, primes = [];
  for (var i = 2; i <= num; i++)
    {
      if (prime(i)) primes.push(i);
    }
  for (i = 0; i <= primes.length - 1; i++) 
    {
      sum += primes[i];
    }
  return sum;
}

sumPrimes(10);

```

There are more solutions. They will be uploaded later.
