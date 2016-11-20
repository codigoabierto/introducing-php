## 3. Making decisions with conditional statements

1. The truth according to PHP
2. Making decisions with conditions and comparisons
3. Alternative syntax for conditional statements
4. Making decisions with a switch statement
5. Using the ternary operator as shorthand
6. Setting a default value
7. Challenge: Serving different content to members
8. Solution: Serving different content to members


### 3.1 The truth according to PHP

###### Making decisions

- Decisions are based on conditions
- A condition must be either true or false
- true and false are boolean values
- Booleans can be implicit or explicit

Explicit Boolean Values

- true
- false

Implicit Boolean values

- Zero as a number or string (0, 0.0, '0')
- An empty string ('', "")
- An empty array ([])
- NULL (including unset variables)
- SimpleXML object created from empty tags


### 3.2 Making decisions with conditions and comparisons

###### Conditional statements

    if (condition is true){
      // do something
    } elseif (second condition is true) {
      // perform alternative task
    } else {
      // do something different
    }

###### Comparison operators

| Operator  | Meaning                   |
| --------- | ------------------------- |
| ==        | Equal                     |
| !=        | Not equal                 |
| ===       | Identical                 |
| !==       | Not identical             |
| <         | Less than                 |
| <=        | Less than or equal to     |
| >         | Greater than              |
| =>        | Greater than or equal to  |

###### Logical Operators

- &&  True if both values are true
- ||  True if either value is true
- ! Reverses the meaning

### 3.3 Alternative syntax for conditional statements

- Opening curly brace is replaced by ":"
- Closing curly brace is ommited, except for the last condition where "endif;" is used
- Both elseif and endif cannot have spaces else\/end and if


    if (condition is true) :
      // do something
    elseif (second condition is true) :
      // perform alternative task
    else :
      // do something different
    endif;

### 3.4 Making decisions with a switch statement

- In comparison to if-else, only the OR operator can be emulated but not the AND operator
- Only number, string or boolean values can be tested
- Only the first condition that evaluates to tru will be used


    switch ( $var ) {
      case value1:
          // do this
          break;
      case $var > value2:
      case value3:
          // do this instead
          break;
      default:
          // do this if nothing else matches
    }

### 3.5 Ternary operator

- It gets its name because it operates with 3 values or expressions

      $var = ( condition ) ? value if true : value if false;
