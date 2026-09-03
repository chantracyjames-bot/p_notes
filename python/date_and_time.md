# Date and Time
 - _date_ class
	- Definition:
		- Used to create and manipulate date objects.
		- When an instance of this class is created, it represents a specific calendar date in ISO 8601 format.
			- YYYY-MM-DD
	- Creating a date object
		- Syntax:
			```
			datetime.date(<year>, <month>, <day>)
			```
			- Where:
				- year
					- An integer between MINYEAR and MAXYEAR.
						- MINYEAR = 1
						- MAXYEAR = 9999
				- month
					- An integer between 1 to 12.
					- 1 is January, 12 is December.
				- day
					- An integer that is valid for the specified montn and year.
					- Do note that on February, it is either 28 or 29 depending on the leap year.
		- Example:
			```
			print(datetime.date(2026, 6, 26)) #> 2026-06-26
			```
		- Note:
			- Entering values that is not an integer will throw a _TypeError_.
			- Providing values larger than MAXYEAR or smaller than MINYEAR, will throw a _ValueError_
			- The date object does not include any time or timezone information, for that, refer to _datetime_.
		- Attributes and methods
			- _.ctime()_
				- Definition:
					- Returns a string representation of the date.
				- Syntax:
					```
					datetime.date.ctime(<datetime.date_object>)
					```
				- Example:
					```
					import datetime

					date_today = datetime.date.today()
					print(datetime.date.ctime(date_today))
					```
	
			- _.isoformat()_
				- Definition:
					- Converts the date into a string format.
			- _.today()_
				- Definition:
					- Returns the date today.
				- Syntax:
					```
					datetime.date.today()
					```