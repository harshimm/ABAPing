# Search 🔍
- Helps to find a character or pattern of characters within the string.
- SEARCH statement does not need variable to store result.
- Variables sy-subrc and sy-fdpos are used to check if the search has executed successfully.
- sy-subrc : indicates if search has executed successfully or not
  - Returns value 0 if successful
  - Returns value 4 if unsuccessful
- sy-fdpos : indicates the postion of that character or pattern found
  - Returns the position of the character according to the scenarios mentioned below
  - Returns 0 if the search is unsuccessful
     
```
DATA str TYPE string.
str = '  Harshini'.
```

### Find character in the string
- Here the spaces in front are also considered while checking position of the character
- So H lies in the 3rd position and sy-fdpos returns 3
```
SEARCH str FOR 'a'.
WRITE sy-subrc.
WRITE sy-fdpos.
```
### Output
```
0 3
```

### Find string within the string
- sy-fdpos returns the position where the string ends
- h in sh is in position 5, so sy-fdpos returns 5
```
SEARCH str FOR 'sh'.
WRITE / sy-subrc.
WRITE sy-fdpos.
```
### Output
```
0 5
```

### Find string within string that contains trailing spaces
- Trailing spaces are ignored for the search
```
SEARCH str FOR 'ini   '.
WRITE / sy-subrc.
WRITE sy-fdpos.
```
### Output
```
0 7
```

### Search using wildcards
- sy-fdpos returns position 2, because it returns the position from where the word that ends with "ini" starts.
- In this case the word is Harshini.
- H is in position 2, hence the value of sy-fdpos = 2
```
SEARCH str FOR '*ini'.
WRITE / sy-subrc.
WRITE sy-fdpos.
```
### Ouput
```
0 2
```

### Meanings of wildcard patterns
- *ch -> Find a word that ends with ch
- ch* -> Find a word that starts with ch
- * ch * -> Find a word that contains ch anywhere in the string. SAP does not support this, as wildcards are not treated as regex patterns here.
 
### Examples that will fail for this string
1. ```
   SEARCH str FOR 'a*'.
   WRITE / sy-subrc.
   WRITE sy-fdpos.
   ```
   ```
   4 0
   ```
2. ```
   SEARCH str FOR '*a'.
   WRITE / sy-subrc.
   WRITE sy-fdpos.
   ```
   ```
   4 0
   ```
3. ```
   SEARCH str FOR '*a*'.
   WRITE / sy-subrc.
   WRITE sy-fdpos.
   ```
   ```
   4 0
   ```
