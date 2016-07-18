## Binary Agents

### Description
Return an English translated sentence of the passed binary string.

The binary string will be space separated.

### Code

```javascript
function binaryAgent(str) {
  var arr = str.split(" ");
  var mystr = "";
  for (var i = 0; i <= arr.length - 1; i++) {
    var tlen = arr[i].length - 1;
    var temparr = arr[i].split("");
    var temp = 0;
    for (var j = 0 ; j <= temparr.length - 1; j++) {
      temp += parseInt(temparr[j]) * Math.pow(2, tlen);
      tlen -= 1;
    }
    mystr += String.fromCharCode(temp);
  }
  return mystr;
}

binaryAgent("01000001 01110010 01100101 01101110 00100111 01110100 00100000 01100010 01101111 01101110 01100110 01101001 01110010 01100101 01110011 00100000 01100110 01110101 01101110 00100001 00111111");
```

There are more solutions. They will be uploaded later.