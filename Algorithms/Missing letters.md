## Missing letters

### Description
Find the missing letter in the passed letter range and return it.

If all letters are present in the range, return undefined.

### Code

```javascript


function fearNotLetter(str) {
  for (var i = 0; i <= str.length - 2; i++) {
    if (str.charCodeAt(i+1) - str.charCodeAt(i) != 1) {
      return String.fromCharCode(str.charCodeAt(i) + 1);
    }
  }
  return undefined;
}

fearNotLetter("abce");
```

There are more solutions. They will be uploaded later.
