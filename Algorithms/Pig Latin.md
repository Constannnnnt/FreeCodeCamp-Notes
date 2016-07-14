## Pig Latin

### Description
Translate the provided string to pig latin.

Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay".

If a word begins with a vowel you just add "way" to the end.

Input strings are guaranteed to be English words in all lowercase.

### Code

```javascript


function translatePigLatin(str) {
  str.toLowerCase();
  var vowel = {"a": 1, "e":2, "i": 3, "o" : 4, "u" : 5};
  if (vowel.hasOwnProperty(str[0])) {
    return str+"way";
  }
  else
  {
    while (!vowel.hasOwnProperty(str[0])) {
      var substr = str.substr(1);
      substr+=str[0];
      str = substr;
    }
    str += "ay";
  }
  return str;
}

translatePigLatin("consonant");
```

There are more solutions. They will be uploaded later.
