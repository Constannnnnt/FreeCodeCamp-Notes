## Caesars Cipher 

### Description
One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

### Code

```javascript
function rot13(str) { // LBH QVQ VG!
  var arr = str.split(" ");
  var strmp = "";
  for (var i = 0 ; i <= arr.length - 1; i++) {
    var temp = arr[i].split("");
    for (var j = 0; j <= temp.length - 1; j++) {
      if (temp[j].charCodeAt(0)>= 65 && temp[j].charCodeAt(0)<= 90)
      {
        if (temp[j].charCodeAt(0)-65 < 13)
          strmp += String.fromCharCode(temp[j].charCodeAt(0)+13);
      else if (temp[j].charCodeAt(0) - 65 >= 13)
          strmp += String.fromCharCode(temp[j].charCodeAt(0)-13);
      }
      else {
        strmp += temp[j];
      }
    }
    strmp += " ";
  }
  strmp = strmp.slice(0, strmp.length - 1);
  return strmp;
}

// Change the inputs below to test
rot13("SERR PBQR PNZC");
/*
rot13("SERR PBQR PNZC") should decode to "FREE CODE CAMP"
rot13("SERR CVMMN!") should decode to "FREE PIZZA!"
rot13("SERR YBIR?") should decode to "FREE LOVE?"
rot13("GUR DHVPX OEBJA QBT WHZCRQ BIRE GUR YNML SBK.") should decode to "THE QUICK BROWN DOG JUMPED OVER THE LAZY FOX."
*/
```

There are more solutions. They will be uploaded later.## Code
