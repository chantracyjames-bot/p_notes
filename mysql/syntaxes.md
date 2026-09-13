
# Syntaxes
### Case-sensitive
- Definition:
	- select and SELECT are the same statement.
### Semicolons
- Definition:
	- Some database systems require a semicolon at the end of each SQL statement.
	- It is the standard way to separate each SQL statement in database systems, allowing for more than one SQL statement to be executed all while in the same call to the server.
### Text vs Numbers
- Text
	- Definition:
		- Like in most programming languages, text or strings are enclosed in single quotes ''.
	- Note
		- Some databases allow double quotes " ".
	- example:
		```
		'idkman'
		```
- Numbers
	- Definition:
		- When dealing with numbers, it does not require any quotations.
	- Example:
		```
		23
		```
### Comments
- Single-line comments
	- Definition:
		- Can be a double dash _--_ or can be a double frontslash _//_, similar to C-style languages.
	- Example:
		```
		-- this is a comment
		// this is a comment
		```
- Multi-line comments
	- Definition:
		- Through the C-style multi-line comment.
	- Example:
		```
		/*
		this is a comment
		*/
		```
### Important SQL commands
- SELECT
	- Extracts data from a database.
- UPDATE
	- Updates data in a database.
- DELETE
	- Deletes data from a database.
- INSERT INTO
	- Inserts new data into a database.
- CREATE DATABASE
	- Creates a new database.
- ALTER DATABASE
	- Alters or modifies a database.
- CREATE TABLE
	- Creates a new table.
- ALTER TABLE
	- Alters of modifies a table
	- Operations are: adding, dropping, renaming, modifying columns, adding constraints, and renaming the table.
- DROP TABLE
	- Deletes a table.
- CREATE INDEX
	- Creates an index or a search key
- DROP INDEX
	- Deletes an index