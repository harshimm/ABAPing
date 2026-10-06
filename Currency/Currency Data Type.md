# Currency Data Type 💲

### Declaration
```
DATA tax TYPE p decimals 2 VALUE '0.15'.
DATA salary TYPE p decimals 2 VALUE '90000'.
DATA deduction TYPE p decimals 2.
DATA base_salary TYPE p decimals 2.
```

### Currency key declaration
- Used to define which currency it is e.g: USD, INR, GBP

```
DATA curr_key type waers value 'inr'.
```

### Sample Calculation
```
deduction = tax * salary.
base_salary = salary - deduction.

WRITE : 'Salary : ', salary, curr_key,
        / 'Tax Percentage : ', tax, curr_key,
        / 'Deduction : ', deduction, curr_key,
        / 'Base Salary : ', base_salary, curr_key.
```

### Output
```
Salary :         90,000.00  inr
Tax Percentage :              0.15  inr
Deduction :         13,500.00  inr
Base Salary :         76,500.00  inr
```
