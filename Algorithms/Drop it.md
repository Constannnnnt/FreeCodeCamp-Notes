## Drop it

### Description
Drop the elements of an array (first argument), starting from the front, until the predicate (second argument) returns true.

The second argument, func, is a function you'll use to test the first elements of the array to decide if you should drop it or not.

Return the rest of the array, otherwise return an empty array.

### Hint

- [Array.prototype.shift()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
- [Array.prototype.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)

### Code

```javascript
function dropElements(arr, func) {
  // Drop them elements.
  var i = 0;
  while (i <= arr.length - 1) {
    if (func(arr[i])) {
      arr=arr.slice(i);
      return arr;
    }
    else {
      arr.shift();
      i=0;
    }
  }
  return arr;
}

dropElements([1, 2, 3], function(n) {return n < 3; });
```

There are more solutions. They will be uploaded later.