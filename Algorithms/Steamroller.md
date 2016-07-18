## Steamroller

### Description
Flatten a nested array. You must account for varying levels of nesting.

### Code

```javascript
function steamrollArray(arr) {
  // I'm a steamroller, baby
  return arr.reduce(function (flat, toFlatten) {
    return flat.concat(Array.isArray(toFlatten) ? steamrollArray(toFlatten) : toFlatten);
  }, []);
}

steamrollArray([1, [2], [3, [[4]]]]);

```

There are more solutions. They will be uploaded later.