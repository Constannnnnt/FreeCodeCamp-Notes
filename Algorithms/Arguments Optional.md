## Arguments Optional

### Description
Create a function that sums two arguments together. If only one argument is provided, then return a function that expects one argument and returns the sum.

For example, addTogether(2, 3) should return 5, and addTogether(2) should return a function.

Calling this returned function with a single argument will then return the sum:

var sumTwoAnd = addTogether(2);

sumTwoAnd(3) returns 5.

If either argument isn't a valid number, return undefined.

### Code

```javascript
function addTogether() {
  var args = Array.prototype.slice.call(arguments);
  var alen = args.length;
  if (alen === 2) {
    if ((typeof args[0] !== "number") || (typeof args[1] !== "number")) return undefined;
    return args[0] + args[1];
  }
  else {
    if (typeof args[0] !== "number") return undefined;
    return function(temp) {
      if ((typeof temp  === "number") && (typeof args[0]  === "number")) return args[0]+temp;
      return undefined;
    };
  }
}
addTogether(2,3);
// addTogether(2)(3) should return 5.
// addTogether("http://bit.ly/IqT6zt") should return undefined.
// addTogether(2, "3") should return undefined.
// addTogether(2)([3]) should return undefined.

```

There are more solutions. They will be uploaded later.## Code
