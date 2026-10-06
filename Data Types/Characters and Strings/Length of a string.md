# Length of a String ➡️
- The function strlen() will be used to find the length of the string.

```
DATA name TYPE string VALUE 'Harshini'.
DATA length TYPE i.
```

### Length of string without spaces

```
length = strlen( name ).
WRITE length.
```

### Output
```
8
```

### Length of String with spaces

#### Adding space after the string will not be considered while calculating the length
```
name = 'Harshini '.
length = strlen( name ).
WRITE length.
```

### Output
```
8
```

#### Adding spaces before the string will be considered while calculating the length

```
name = ' Harshini'.
length = strlen( name ).
WRITE length.
```

### Output
```
9
```
