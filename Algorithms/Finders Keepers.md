## Finders Keepers

### Description
Create a function that looks through an array (first argument) and returns the first element in the array that passes a truth test (second argument).

### Code

```javascript
function findElement(arr, func) {
  var num = arr.filter(func);
  if (num[0]) return num[0];
  else return undefined;
}

findElement([1, 2, 3, 4], function(num){ return num % 2 === 0; });

```

There are more solutions. They will be uploaded later.
