# Replace Characters ↔️
- Used to replace any character in the string
- Replaces only the first occurrence of the string
- To replace multiple occurrences a WHILE loop needs to be used

```
DATA str TYPE string.
str = 'Hello,World,'
```

### Replace single occurrence
```
REPLACE ',' WITH '.' IN str.
WRITE str.
```
### Output
```
Hello.World,
```

### Replace multiple occurences

```
WHILE sy-subrc = 0.
  REPLACE ',' WITH '.' IN str.
ENDWHILE.

WRITE str.
```

### Output
```
Hello.World.
```
