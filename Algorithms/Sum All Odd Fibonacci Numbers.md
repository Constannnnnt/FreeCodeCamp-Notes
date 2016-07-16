## Sum All Odd Fibonacci Numbers

### Description
Given a positive integer num, return the sum of all odd Fibonacci numbers that are less than or equal to num.

The first two numbers in the Fibonacci sequence are 1 and 1. Every additional number in the sequence is the sum of the two previous numbers. The first six numbers of the Fibonacci sequence are 1, 1, 2, 3, 5 and 8.

For example, sumFibs(10) should return 10 because all odd Fibonacci numbers less than 10 are 1, 1, 3, and 5.

### Code

```javascript

function fib(num) {
  var arr = [1,1];
  while (arr[arr.length - 1] <= num)
    {
      var temp = arr[arr.length - 1] + arr[arr.length - 2];
      arr.push(temp);
    }
  console.log(arr);
  var sum = 0;
  for (var i = 0; i <= arr.length - 1; i++) {
    if ((arr[i] % 2) && arr[i]<=num) sum += arr[i];
  }
  return sum;
}

function sumFibs(num) {
  var sum = fib(num);
  return sum;
}

sumFibs(4);
```

There are more solutions. They will be uploaded later.
