## Diff Two Arrays

### Description
Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.

### Hint
- [Comparison Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators)
- [Array.prototype.slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
- [Array.prototype.filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [Array.prototype.indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
- [Array.prototype.concat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)

### Code

```javascript
function diffArray(arr1, arr2) {
  var newArr = [];
  // Same, same; but different.
  for (var i = 0 ; i <= arr1.length - 1; i++) {
    if (arr2.indexOf(arr1[i]) === -1) newArr.push(arr1[i]);
  }
  for (var j = 0 ; j <= arr2.length - 1; j++) {
    if (arr1.indexOf(arr2[j]) === -1) newArr.push(arr2[j]);
  }
  return newArr;
}
diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```

There are more solutions. They will be uploaded later.
