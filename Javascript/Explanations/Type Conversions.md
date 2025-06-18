### Type Conversions

1. When we are adding any 2 types of distinct data in javascript, if one of the data is string then other data whatever maybe will convert to string
   1. Ex: 10 + "20" - 1020 ; true + "20" - true20
2. Whereas when we are doing any other mathematical operations on distinct data, then string is converted to number and then operations are performed.
   1. Ex: 10 - "20" -> -10 ; true - "20" -> -19
   2. Ex: 10 \* "20\* -> 200
   3. Ex: 20 / "10" -> 2
   4. Ex: 20 % "10" -> 0
3. Boolean values are converted everytime, with strings and with numbers. True : 1 and False : 0
   1. True + "10" - 11
   2. False - 10 -> -10
4. Also there are two types of conversions: Implicit Type/Automatic Type, Explicit Type