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
  var alen = arguments.length;
  if ((typeof(arguments[0]) !== "number") || (typeof(arguments[1]) !== "number")) {
    return undefined;
  }
  if (alen === 2) {
    return arguments[0] + arguments[1];
  }
  else {
    return function(w) {
      if (typeof(w) !== "number") return undefined;
      return arguments[0]+w;
    };
  }
}

addTogether(2,3);

```

There are more solutions. They will be uploaded later.## Code
