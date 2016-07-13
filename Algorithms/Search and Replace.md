## Search and Replace

### Description
Perform a search and replace on the sentence using the arguments provided and return the new sentence.

First argument is the sentence to perform the search and replace on.

Second argument is the word that you will be replacing (before).

Third argument is what you will be replacing the second argument with (after).

NOTE: Preserve the case of the original word when you are replacing it. For example if you mean to replace the word "Book" with the word "dog", it should be replaced as "Dog"

### Hint
- [Array.prototype.splice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
- [String.prototype.replace()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace)
- [Array.prototype.join()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)

### Code

```javascript

function myReplace(str, before, after) {
  var arr = str.split(" ");
  for (var i = 0 ; i <= arr.length - 1; i++) {
    if (arr[i] === before) {
      if (before[0] < 'a') {
        after = after.replace(after[0], after[0].toUpperCase());
      }
      arr[i] = after;
    }
  }
  str = arr.join(" ");
  return str;
}

myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");

```

There are more solutions. They will be uploaded later.
