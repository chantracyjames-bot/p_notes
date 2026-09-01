
# Operators
- Definition:
	- Used to manipulate data or variable.
	- Has five types; Arithmetic, Assignment, Comparison, Logical, Precedence

- Arithmetic
	- Definition:
		- Commonly used for mathematical operations.
	- Types or arithmetic operators:
		- Addition (_+_)
			- Definition:
				- Used to add two values if and only if they have the same data type.
			- Note:
				- Adding numeric types and non-numeric types results into errors.
			- Example: 
				```
				sum: int = 10 + 15 #> 25
				```
		- Subtraction (_-_)
			- Definition:
				- Subtracts two values from one another.
			- Example: 
				```
				dif: int = 10 - 15 #> -5
				```
		- Multiplication (_\*_)
			- Definition:
				- Multiplies two values with each other.
			- Example: 
				```
				pro: int = 10 * 15 #> 150
				```
		- Division (_/_)
			- Definition:
				- Divides one value by the other.
			- Example: 
				```
				quo: int = 10 / 15 #> 0.666666666666 (auto casts to float)
				```
		- Modulus (_%_)
			- Definition:
				- Returns the division remainder
			- Example: 
				```
				mod: int = 10 % 15 #> 5
				```
		- Exponentiation (_\*\*_)
			- Definition:
				- Raises a value to an exponent
			- Example:
				```
				exp: int = 10 ** 15 #> 100
				```
		- floor division (_//_)
			- Definition:
				- Divides one value by the other and takes the highest integer lower than the result.
			- Example:
				```
				flo: int = 10 // 15 #> 0   
				```  

- Assignment
	- Definition
		- Used to assign values to variables.
	- Types of assignment operators:
		- Assignment operator (_=_)
			- Definition:
				- Used to assign any values to variables.
				- It is also used to initialize variables with values.
			- Example: 
		- Addition assignment (_+=_)
			- Definition
				- Used to increment (or add) values.
			- Example: 
				```
				10 += 10 #> 20
				```
		- Subtraction assignment (_-=_)
			- Definition:
				- Used to decrement (or subtract) values.
			- example: 
				```
				10 -= 10 #> 0
				```
		- Multiplication assignment (_\*=_)
			- Definition:
				- Used to multiply values.
			- Example: 
				```
				10 *= 10 #> 100
				```
		- Division assignment (_\/\=_)
			- Definition:
				- Used to divide values.
			- Example: 
				```
				10 /= 10 #> 1
				```
		- Modulo assignment (_%=_)
			- Definition:
				- Used to retrieve remainder values.
			- Example: 
				```
				10 %= 10; #> 0
				```
		- Floor division assignment (_\/\/\=_)
			- Definition
				- Used to divide values, it returns a value rounded down.
			- Example:
				```
				10 //= 10 #> 1
				```
		- Exponential assignment (**=)
			- Definition:
				- Used to raise values to an exponent.
			- Example:
				```
				10 **= 3 #> 100
				```
		- Bitwise AND assignment (_\&\=_)
			- Definition:
				- Used for bitwise operations, using the AND logic comparisons.
			- Example: 
				```
				a: int = 60       #> 0011 1100
				b: int = 13       #> 0000 1101
				a &= b            #> 0000 1100 - 12 in binary
				```
		- Bitwise OR assignment (_\|\=_)
			- Definition:
				- Used for bitwise operations, using the OR logic comparisons.
			- Example: 
				```
				a: int = 60;      #> 0011 1100
				b: int = 13;      #> 0000 1101
				a |= b;           #> 0011 1101 - 61 in binary
				10 %= 10 #> 0
				```
		- Bitwise XOR assignment (_\^\=_)
			- Definition
				- Used for bitwise operations, using the XOR logic comparisons.
			- Example: 
				```
				a: int = 60;      #> 0011 1100
				b: int = 13;      #> 0000 1101
				a &= b;           #> 0011 0001 - 49 in binary
				10 ^= 10 #> 0
				```
		- Left-shift assignment (_\<\<\=_)
			- Definition:
				- Shifts the bit to the left, which effectively multiplies the value by 2^n.
			- Example: 
				```
				60 <<= 2     #> 1111 0000 - 240 in binary
				```
		- Right-shift assignment (_\>\>\=_)
			- Definition:
				- Shifts the bit to the right, which effectively divides the value by 2^n.
			- Example: 
				```
				60 >>= 2     #> 0000 1111 - 15 in binary
				```
		- Walrus assignment (_\:\=_)
			- Definition:
				- Assigns values to a variable.
			- Example:
				```
				count := 10        #> count = 10
				#> or
				print(count := 10) #> count = 10
				#> print(count)
				```

- Comparison
	- Definition:
		- Used to compare two values, returning a Boolean.
		- Returns either a _True_ or a _False_, or either 1 or 0.
	- Types of comparison operators:
		- Equal to (_\=\=_)
			- Definition:
				- Returns a _True_ if both values are equal, a _False_ otherwise.
			- Example: 
				```
				10 == 10 #> True
				```
		- Not equal to (_\!\=_)
			- Definition:
				- Returns a _True_ if the values are not equal, returns a _False_ if they are equal.
			- Example: 
				```
				10 != 5 #> True
				```
		- Greater than (_>_)
			- Definition:
				- Returns a _True_ if the value to the left if greater than the value in the right.
			- Example: 
				```
				10 > 5 #> True
				```
		- Less than (_<_)
			- Definition
				- Returns a _True_ if the value to the left if less than the value in the right.
			- Example: 
				```
				10 < 5 #> False
				```
		- Greater than or equal to (_>\=_)
			- Definition:
				- Returns a _True_ if the value to the left if greater than or equal to the value in the right
			- Example: 
				```
				10 >= 5 #> True
				```
		- Less than or equal to (_<\=_)
			- Definition:
				- Returns a _True_ if the value to the left if less than or equal to the value in the right
			- Example: 
				```
				5 <= 5 #> True
				```

- Logical
	- _not_
		- Definition
			- Logical negation.
			- Flips the truth value of a boolean.
		- Example:
			```
			"World" not in "Hello World" #> False
			```
	- _and_ 
		- Definition:
			- Logical AND.
			- Chains multiple conditions and returns a _True_ if and only if all the conditions are _True_.
		- Example:
			```
			10 > 5 and 19 < 20 #> True
			```
	- _or_
		- Definition:
			- Logical OR.
			- Chains multiple conditions and returns a _True_ if and only if one condition is _True_.
		- Example:
			```
			10 > 15 or 5 > 0 #> True
			```

- Identity
	- _is_
		- Definition:
			- Returns a _True_ if both values are the same object,
		- Note:
			- _is_ and _\=\=_ are not the same
			- _is_ queries if both objects refer to the same object in memory.
			- _\=\=_ queries if both the objects contain the same elements.
		- Example:
			```
			"idkman" is "idkman" #> _True_
			```
	- _is not_
		- Definition:
			- Returns a _True_ if both values are not the same object.
		- Example:
			```
			"idkman" is not "Hello World" #> _True_
			```

- Membership
	- _in_
		- Definition:
			- Queries if a certain value is inside of a larger array of values, or if a certain string is inside of a larger array of strings.
			- Returns a bool value, either a _True_ or a _False_.
		- Example:
			```
			"Hell" in "Hello World" #> _True_
			```
	- _not in_
		- Definition:
			- Queries if a certain value is not inside of a larger array of values, or if a certain string is not inside of a larger array of strings.
			- Returns a bool value, either a _True_ or a _False_.
		- Example:
			```
			"idkman" in "Hello World" #> True
			```

- Bitwise
	- Bitwise AND (_&_)
		- Definition:
			- Sets each bit to 1 if both bits are 1.
		- Example:
			```
			6 & 3 #> 2
			6 = 0000000000000110
			3 = 0000000000000011
			^ 
			0000000000000010 - value of 2
			```
	- Bitwise OR (|)
		- Definition:
			- Sets each bit to 1 if one of two bits are 1.
		- Example:
			```
			6 | 3 #> 7
			6 = 0000000000000110
			3 = 0000000000000011
			^^^
			0000000000000111 - value of 7
			```
	- Bitwise XOR (^)
		- Definition:
			- Sets each bit to 1 if only one of two bits are 1.
		- Example:
			```
			6 ^ 3 #> 5
			6 = 0000000000000110
			3 = 0000000000000011
			^ ^
			0000000000000101 - value of 5
			```
	- Bitwise NOT (~)
		- Definition:
			- Inverts all bits.
		- Example:
			```
			~3 #> -4
			3 = 0000000000000011
			1111111111111100 - value of -65532
			```
	- Zero fill left shift (<<)
		- Definition:
			- Pushes all zeros to the left, discarding the leftmost bits.
		- Example:
			```
			3 << 2 #> 12
			3 = 0000000000000011
			0000000000001100 - value of 12
			```
	- Signed right shift (<<)
		- Definition:
			- Pushes all zeros to the right, discarding the rightmost bits.
		- Example:
			```
			12 >> 2 #> 3
			12 = 0000000000001100
			0000000000000011 - value of 
			```

- Precedence
	- Definition
		- It is the order of operations, similar of PEMDAS in mathematics–from left to right.
		- If two similar level in precedence operators are in the same equation, precedence starts from the left to right.
	- Operator precedence:

		| Name  | Symbol  |
		| :---: | :---: |
		| Parentheses |  ()  |
		| Exponents |  **  |
		| Unary Plus, Minus, <br>and Bitwise NOT    |  +x, -x, ~x  |
		| Multiplication, <br>Division, and Modulus |    \*, /, //, %*  |
		| Adding and Subtracting  |   +, -  |
		| Bitwise Left and <br>Right Shifts  |  <<, >>   |
		| Bitwise AND   |   &    |
		| Bitwise XOR |  ^    |
		| Bitwise OR|      \|    |
		| Comparisons, Identity, <br>and Membership | \=\=, !\=, >, <, <br>>\=, <\=, is,<br>is not, in, not in |
		| Logical NOT  |      not    |
		| Logical AND  |      and     |
		| Logical OR  |     or  |

- Other Operators
	- Shorthand statements
		- Ternary operators
			- Definition:
				- Short version of an _if-else_ statement.
			- Syntax:
				```
				<statement> if <condition> else <statement>
				```
			- Example:
				```
				print("yes") if 10 == 10 else print("no")
				```
		- Nested ternary operator
			- Definition:
				- An extended version of the regular ternary operator, includes the _elif_ conditional statement.
			- Syntax:
				```
				<statement> if <condition> else <statement> if <condition> else <statement>
				``` 
			- Example:
				```
				print("no") if 10 == 20 else print("maybe") if 10 == 15 else print("yes")
				```
	- Set operators
		- Definition:
			- Operators that are only applicable when used on sets.
		- Operators: 
			- union operator (_|_)
				- Definition:
					- An alternative to the .union() method.
				- Syntax:
					```
					<set_name1> | <set_name2>
					```
			- intersection operator (_&_)
				- Definition:
					- An alternative to the .intersection() method.
				- Syntax:
					```
					<set_name1> & <set_name2>
					```
			- difference operators (-)
				- Definition:
					- An alternative to the .difference() method.
				- Syntax:
					```
					<set_name1> - <set_name2>
					```
			- symmetric difference operator (^)
				- Definition:
					- An alternative to the .symmetric_difference() method.
				- Syntax:
					```
					<set_name1> ^ <set_name2>
					```