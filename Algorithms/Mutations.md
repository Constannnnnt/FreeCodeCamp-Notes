## Mutations

### Description
Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

For example, ["hello", "Hello"], should return true because all of the letters in the second string are present in the first, ignoring case.

The arguments ["hello", "hey"] should return false because the string "hello" does not contain a "y".

Lastly, ["Alien", "line"], should return true because all of the letters in "line" are present in "Alien".

### Code

```javascript
function mutation(arr) {
  arr[0] = arr[0].toLowerCase();
  arr[1] = arr[1].toLowerCase();
  if (arr[0].length >= arr[1].length){
     var splitArr = arr[1].split("");
     for (var i = 0 ; i <= splitArr.length - 1; i++)
     {
       if (arr[0].indexOf(splitArr[i]) === -1) return false; 
     }
  } else {
    var splitArr = arr[0].split("");
    for (var i = 0 ; i <= splitArr.length - 1; i++)
     {
       if (arr[1].indexOf(splitArr[i]) === -1) return false; 
     }
  }
  return true;
}
mutation(["hello", "hey"]);
/*
mutation(["hello", "hey"]) should return false.
mutation(["hello", "Hello"]) should return true.
mutation(["zyxwvutsrqponmlkjihgfedcba", "qrstu"]) should return true.
mutation(["Mary", "Army"]) should return true.
mutation(["Mary", "Aarmy"]) should return true.
mutation(["Alien", "line"]) should return true.
mutation(["floor", "for"]) should return true.
mutation(["hello", "neo"]) should return false.
mutation(["voodoo", "no"]) should return false.
*/
```

There are more solutions. They will be uploaded later.## Code
