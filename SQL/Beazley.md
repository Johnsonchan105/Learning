# Beazley's Last Statment

### A First SQL Inquiry

- find first 3 rows of the execution table

``` SQL
1. SELECT * FROM executions LIMIT 3
```

### The SELECT Block

- specifies which columns you want to output
- format:
  - `SELECT <column>, <column>, ...`
  - each column must be seperated from a comma
    - space following optional
  - `*` - want all columns in the table

### The FROM Block

- specifies which table querying from
- format:
  - `FROM <table>`
  - always comes after the SELECT block
- no need for FROM block if not using anything from a table
- ex:
  - `SELECT first_name FROM executions LIMIT 3`

to do decimal division, one of the operands must be a decimal or multiply one number by 1.0

### The WHERE Block

- filter table for rows that meet certain conditions
- format:
  - `WHERE <clause>`
    - clause is a bool statement
      - ex: `ex_number = 145`
  - always goes after the `FROM` block
  - ex:
    - find first and last names and ages (ex_age) of inmates 25 or youngerat the time of execution
    - `SELECT first_name, last_name, ex_age FROM executions WHERE ex_age <= 25`
    - 
#### `LIKE` keyword
- use % and _ to match various characters
- ex:
  - first_name LIKE '%roy'
    - returns true for rows with first names 'roy , 'Troy', 'Deroy' but not 'royman'
  - wildcard '_roy'
    - matches only for single character so only 'Troy' will match
- ex:
  - find results for Raymond Landry  
 
 ```SQL 
 SELECT first_name, last_name, ex_number 
 FROM executions
 WHERE first_name = 'Raymond'
        AND last_name LIKE '%Landry%'
 ```

 Boolean Operators: `NOT, AND, OR`  
1 = true, 0 = false

Final Example:
find Napoleon Beazley's last statement  
```SQL
SELECT last_statement
FROM executions
WHERE first_name = 'Napoleon' AND last_name = 'Beazley'
```