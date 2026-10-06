# CONCATENATE STRINGS 🤝 🔤

### 1. Join strings without separator
   
```
data: word1 type string value 'Hello',
      word2 type string value 'World',
      sep,
      result type string.

CONCATENATE word1 word2 into result.
write result.
uline.
```
### Output
```
HelloWorld
```

### 2. Join strings by default separators
- In abap the default data type is character
- The variable sep would be a character of length 1 by default
- It would be a space by default.

```
concatenate word1 word2 into result SEPARATED BY sep.
write / result.
uline.
```
### Output
```
Hello World
```

### 3. Join strings with a specific separator

- Sep is assigned a value and used for concatenation

```
sep = ','.

concatenate word1 word2 into result separated by sep.

write / result.
uline.
```
### Output
```
Hello,World
```
