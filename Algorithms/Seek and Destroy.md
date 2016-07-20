## Seek and Destroy

### Description
You will be provided with an initial array (the first argument in the destroyer function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments.

### Code

```javascript
function validate(value) {
  if (value !== "") return value;
}

function destroyer(arr) {
  // Remove all the values
  for (var i = 1; i <= arguments.length - 1; i++) {
    for (var j = 0; j <= arr.length - 1; j++) {
      if (arr[j] === arguments[i]) arr[j] = "";
    }
  }
  arr = arr.filter(validate);
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
/*
destroyer([1, 2, 3, 1, 2, 3], 2, 3) should return [1, 1].
destroyer([1, 2, 3, 5, 1, 2, 3], 2, 3) should return [1, 5, 1].
destroyer([3, 5, 1, 2, 2], 2, 3, 5) should return [1].
destroyer([2, 3, 2, 3], 2, 3) should return [].
destroyer(["tree", "hamburger", 53], "tree", 53) should return ["hamburger"].
*/
```

There are more solutions. They will be uploaded later.## Code
