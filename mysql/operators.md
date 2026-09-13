
# Operators
### AND
- Definition
	- A statement will run if all conditions are true, if not, it does not run at all.
	- The _WHERE_ clause can contain one or more _AND_ operators.
	- The _AND_ operator is used to filter records, based on more than one condition.
- Note:
	- This operator is able to be chained with the _OR_ operator.
- Syntax:
	```
	SELECT <column> FROM <table_name>
	WHERE <condition1> AND <condition2>;
	```
- Example:

	```
	SELECT * FROM programming
	WHERE language = 'sql' AND some_number = 1; -- runs if noth are true
	```
### OR
- Definition:
	- A statement will run if one of the conditions is true, if none are true, it does not run at all.
	- The _WHERE_ clause can contain one one more _OR_ operators
	- The _OR_ operator is used to filter records based on more than one condition.
- Note:
	- This operator is able to be chained with the _AND_ operator.
		- Example:
			```
			SELECT * FROM programming
				WHERE languages = 'java' AND (some_number = 1 OR some_number = 2);
			```
- Syntax:
```
SELECT <column> FROM <table_name>
WHERE <condition1> OR <condition2>;
```
- Example:
```
SELECT * FROM programming
WHERE language = 'sql' OR some_number = 1; -- runs if either are true
```
### BETWEEN
- Definition:
	- Used to select values within a specified range, the range is inclusive.
	- The beginning and the end values of the range is included
	- Commonly used in a _WHERE_ clause, and the values can be numbers, text, or dates.
	- Functions as a shorthand for multiple _AND_ conditions, making queries shorter and more readable
	- It can also be used with the _NOT_ operator.
- Syntax:
```
-- BETWEEN
SELECT <column/s>
FROM <table_name>
WHERE <column> BETWEEN <value1> AND <value2>;

-- NOT BETWEEN
SELECT <column/s>
FROM <table_name>
WHERE <column> NOT BETWEEN <value1> AND <value2>;
```
### EXISTS
- Definition:
	- Used to check whether a sub-query returns any rows.
	- Evaluates to _TRUE_ if the sub-query returns at least one row, returns _FALSE_ otherwise.
	- Commonly used in a _WHERE_ clause, and can be used with the _NOT_ operator.
- Syntax:
```
-- EXISTS
SELECT <column/s>
FROM <table_name>
WHERE EXISTS (<subquery>);

-- NOT EXISTS
SELECT <column/s>
FROM <table_name>
WHERE NOT EXISTS (<subquery>);
```
### IN
- Definition:
	- Used to check if a specified column's value matches any value in a provided list
	- Commonly used in a _WHERE_ clause, can be combined with the _NOT_ operator.
	- Functions as a shorthand for multiple _OR_ conditions, making queries shorter and more readable.
- Syntax:
```
-- IN
SELECT <column/s>
FROM <table_name>
WHERE <column> IN (<values>);

-- NOT IN
SELECT <column/s>
FROM <table_name>
WHERE <column> NOT IN (<values>);
```
### LIKE
- Definition:
	- Used to search for a specified pattern within a column's text data
	- Commonly used in the _WHERE_ clause, can be combined with the _NOT_ operator
	- Has two wildcards:
		- _%_
			- Percent sign.
			- Represents zero, one, or multiple characters.
		- *_*
			- Underscore sign.
			- Represents a single character.
- Note:
	- Wildcards are able to be used together.
- Syntax:
```
-- LIKE
SELECT <column/s>
FROM <table_name>
WHERE <column> LIKE <pattern>;

-- NOT LIKE
SELECT <column/s>
FROM <table_name>
WHERE <column> NOT LIKE <pattern>;
```
### NOT
- Definition:
	- Negates any condition to the opposite expression.
	- If the condition is true, _NOT_ will make it false
	- The _WHERE_ clause can contain one or more _NOT_ operators and can be used in combination with other operators.
- NOT equals
	- Rejects values that are equal to the condition.
	- Syntax:
		```
		WHERE NOT <column> = <value>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT language = 'sql'; -- returns anything but 'sql' related
		```
- NOT greater than
	- Rejects values that are greater than the value.
	- Syntax:
		```
		WHERE NOT <column> > <value>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT some_number > 4; -- returns anything but numbers greater than 4
		```
- NOT greater than or equal to
	- Rejects values that are greater than or equal to the value.
	- Syntax:
		```
		WHERE NOT <column> >= <value>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT some_number >= 4; -- returns anything but numbers greater than or equal to 4
		```
- NOT less than
	- Rejects values that are less than the value.
	- Syntax:
		```
		WHERE NOT <column> < <value>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT some_number < 5; -- returns anything but numbers less than 5
		```
- NOT less than or equal to
	- Rejects values that are less than or equal to the value.
	- Syntax:
		```
		WHERE NOT <column> <= <value>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT some_number <= 5; -- returns anything but numbers less than or equal to 5
		```
- NOT LIKE
	- Rejects values that matches the _LIKE_ operator.
	- Syntax:
		```
		WHERE <column> NOT LIKE <pattern>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE languages NOT LIKE '%on%'; -- returns anything but entries with 'on' inbetween
		```
- NOT OR
	- Rejects values that are included in the _OR_ operator.
	- Syntax:
		```
		WHERE NOT <condition1> OR NOT <condition2>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE some_number >= 9 OR some_number <= 10;
		```
- NOT BETWEEN
	- Rejects values that are between the _BETWEEN_ operator.
	- Syntax:
		```
		WHERE <column> NOT BETWEEN <value1> AND <value2>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE some_number NOT BETWEEN 9 AND 10;
		```
- NOT AND
	- Rejects values that are included in the _AND_ operator.
	- Syntax:
		```
		WHERE NOT <condition1> AND NOT <condition2>;
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT languages = 'c' AND languages = 'c++';
		```
- NOT IN
	- Rejects values that are inside the _IN_ operator.
	- Syntax:
		```
		WHERE <column> NOT IN (<values>);
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE languages NOT IN ('c', 'c++') -- returns anything but entries that are 'c' or c++
		```
- IS NOT NULL
	- Rejects the absence of value in a field.
	- Syntax:
		```
		WHERE <column> IS NOT NULL:
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE languages IS NOT NULL;
		```
- NOT EXISTS
	- Flips the resulting boolean value returned by the _EXISTS_ operator.
	- Syntax:
		```
		WHERE NOT EXISTS (<subquery>);
		```
	- Example:
		```
		SELECT * FROM programming
		WHERE NOT EXISTS (SELECT some_number FROM programming);
		```