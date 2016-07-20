## Falsy Bouncer

### Description
Remove all falsy values from an array.

Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.

### Code

```javascript
function validate(value) {
  var temp = [false, null, 0, NaN, undefined, ""];
  var flag= true;
  for (var i =0; i<=temp.length -1 ; i++) {
    if (temp[i] === value) flag=false;
  }
  if (flag) return value;
}

function bouncer(arr) {
  // Don't show a false ID to this bouncer.
  var myArr = arr.filter(validate);
  return myArr;
}

bouncer([7, "ate", "", false, 9]);
/*
bouncer([7, "ate", "", false, 9]) should return [7, "ate", 9].
bouncer(["a", "b", "c"]) should return ["a", "b", "c"].
bouncer([false, null, 0, NaN, undefined, ""]) should return [].
bouncer([1, null, NaN, 2, undefined]) should return [1, 2].
*/
```

There are more solutions. They will be uploaded later.## Code
