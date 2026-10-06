# Split strings ↔️
- Divides the string into individual strings/characters based on a separator.

```
DATA : main_string TYPE string VALUE 'HAR**SH**INI',
       separator TYPE string VALUE '**',
       split1 TYPE string.
       split2 TYPE string.
       split3 TYPE string.
```
## Divide string without remainder

1. ```
   SPLIT main_string AT separator INTO split1 split2 split3.
   
   WRITE: / split1,
       / split2,
       / split3.
   ```
### Output
```
HAR
SH
INI
```

2. ```
   main_string = 'HAR** SH**INI'.
   
   SPLIT main_string AT separator INTO split1 split2 split3.

   WRITE: / split1,
       / split2,
       / split3.
   ```
### Ouput
```
HAR
 SH
INI
```

## Divide string with remainder
1. ```
   main_string = 'HAR** SH**INI**'.

   SPLIT main_string AT separator into split1 split2 split3.

   WRITE: / split1,
       / split2,
       / split3.
   
   ```

### Output
```
HAR
 SH
INI**
```

2. ```
   main_string = 'HAR** SH**INI**'.

   SPLIT main_string AT separator into split1 split2.

   WRITE: / split1,
       / split2.
   
   ```

### Output

```
HAR
 SH**INI**
```
