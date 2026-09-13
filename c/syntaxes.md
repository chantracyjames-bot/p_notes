
# Syntaxes
## Statements
- Definition:
	- A statement is a single line (or compound) that performs a single operation, i.e. calling a function, initializing a variable, declaring a loop, etc.
- Note:
	- Every statement must end with a semicolon _;_.
- Example:
```
char my_string[] = "Hello World"; // declaring a variable
printf("%s", my_string); // print statement
```
## Comments
- Definition:
	- Comments in C is done by declaring a double frontslash //
- Note:
	- Comments are not compiled into code.
- Syntax:
```
// <comment>
```
- Example:
```
// comment here
```
## Case-sensitive
- Definition:
	- C is case-sensitive when it comes to naming.
	- true and True are not the same thing.
## Numbers and text
- Strings and Text
	- Definition:
		- Text in C must be wrapped in double quotes _" "_.
		- A single character (char) is usually wrapped in single quotes _' '_.
	- Example:
		```
		char my_string[] = "idkman" // string
		char my_char = 'Z' // char
		```
- Numbers
	- Definition:
		- Numbers doesn't need to be inside quotations, doing so will convert the number into a string.
	- Example:
		```
		int my_num = 100 // int
		int my_float = 3.14 // floats
		```
## Scope
- Code blocks
	- Definition:
		- Blocks or groups of code are often encased in curly braces _{ }_.
		- It is recommended to encase blocks of code that is connected to each other in code blocks to group them.
		- An example is an if, else if, else statements, and even in iterative statements.
	- Note:
		- Without a code block, only the first line will get executed as part of the statement and any succeeding lines will get ignored or get executed outside of the statements.
			- Example:
				```
				if (true)
					printf("yes") // gets executed
					printf("no") // does not get executed
				```
## Naming conventions
- Definition:
	- There are industry standard when naming certain elements in C
- Variables
	- Definition:
		- Usually in snake_case.
	- Example:
		```
		int my_string;
		char my_num[];
		```
- Functions
	- Definition:
		- Usually in snake_case.
	- Example:
		```
		my_function();
		sum_all();
		```
- Filenames and folders
	- Definition:
		- Usually in snake_case.
	- Example:
		```
		my_program.c
		idkman.c
		```
- Enums
	- Definition:
		- Usually in snake_case
	- Example:
		```
		enum my_enum {...}
		enum constants_enum {...}
		```
- Pointers
	- Definition:
		- Usually in snake_case with a prefix of p_.
	- Example:
		```
		int *p_num_ptr;
		
		float *p_idk_ptr;
		```
- Structs
	- Definition:
		- Usually in snake_case with a suffix of \_t or \_s.
	- Example:
		```
		struct my_struct_t {...}
		typedef struct idkman_s {...}
		```
- Constants (const) and enum values
	- Definition:
		- Since enum values are similar to const variables, both follow the SCREAMING_SNAKE_CASE.
	- Example:
		```
		const MY_VAR;
		enum my_enum {
			IDKMAN,
			LUMBAGO
		}
		```
# Scope
- Defintion:
	- By default, the compiler compiles code from the top to bottom, first line until the last line.
	- Calling a variable that is not defined until later in the code will throw an error
		- Example:
			```
			printf(x + 10); -> Error
			int x = 10; // defined later while called before declared
			```
- Block scope
	- Definition:
		- Are statements inside a block of code, variables inside a block scope only exists inside that code block.
		- Trying to access a variable inside a block scope from the outside will throw an error.
	- Example:
		```
		If (true) {
			int x = 10;
		}
		printf("%d", x) -> Error
		```
- Loop scope
	- Definition:
		- Like block scope, variables inside a loop (e.g. for loops) are only accessible inside of it.
		- Trying to access it outside the code block will throw an error.
	- Example:
		```
		while(true) {
			int i = 10;
			break;
		}
		printf("%d", i) -> Error
		```
## Escape sequences
- \n
	- The most common escape sequence, it represents a new line.
- \t
	- It represents a horizontal tab rule.
- \\\
	- Represents a single backslash as text.
- \\"
	- Represents a double quote as text.
## ASCII Printable Characters
- Char Number Description
	- 0 - 31 Control characters
	-   32 space
	- ! 33 exclamation mark
	- " 34 quotation mark
	- \# 35 number sign
	- $ 36 dollar sign
	- % 37 percent sign
	- & 38 ampersand
	- ' 39 apostrophe
	- ( 40 left parenthesis
	- ) 41 right parenthesis
	- * 42 asterisk
	- + 43 plus sign
	- , 44 comma
	- - 45 hyphen
	- . 46 period
	- / 47 slash
	- 0 48 digit 0
	- 1 49 digit 1
	- 2 50 digit 2
	- 3 51 digit 3
	- 4 52 digit 4
	- 5 53 digit 5
	- 6 54 digit 6
	- 7 55 digit 7
	- 8 56 digit 8
	- 9 57 digit 9
	- : 58 colon
	- ; 59 semicolon
	- < 60 less-than
	- = 61 equals-to
	- \> 62 greater-than
	- ? 63 question mark
	- @ 64 at sign
	- A 65 uppercase A
	- B 66 uppercase B
	- C 67 uppercase C
	- D 68 uppercase D
	- E 69 uppercase E
	- F 70 uppercase F
	- G 71 uppercase G
	- H 72 uppercase H
	- I 73 uppercase I
	- J 74 uppercase J
	- K 75 uppercase K
	- L 76 uppercase L
	- M 77 uppercase M
	- N 78 uppercase N
	- O 79 uppercase O
	- P 80 uppercase P
	- Q 81 uppercase Q
	- R 82 uppercase R
	- S 83 uppercase S
	- T 84 uppercase T
	- U 85 uppercase U
	- V 86 uppercase V
	- W 87 uppercase W
	- X 88 uppercase X
	- Y 89 uppercase Y
	- Z 90 uppercase Z
	- \[ 91 left square bracket
	- \ 92 backslash
	- ] 93 right square bracket
	- ^ 94 caret
	- _ 95 underscore
	- \` 96 grave accent
	- a 97 lowercase a
	- b 98 lowercase b
	- c 99 lowercase c
	- d 100 lowercase d
	- e 101 lowercase e
	- f 102 lowercase f
	- g 103 lowercase g
	- h 104 lowercase h
	- i 105 lowercase i
	- j 106 lowercase j
	- k 107 lowercase k
	- l 108 lowercase l
	- m 109 lowercase m
	- n 110 lowercase n
	- o 111 lowercase o
	- p 112 lowercase p
	- q 113 lowercase q
	- r 114 lowercase r
	- s 115 lowercase s
	- t 116 lowercase t
	- u 117 lowercase u
	- v 118 lowercase v
	- w 119 lowercase w
	- x 120 lowercase x
	- y 121 lowercase y
	- z 122 lowercase z
	- { 123 left curly brace
	- | 124 vertical bar
	- } 125 right curly brace
	- ~ 126 tilde