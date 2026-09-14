
# Date and Time
- Definition:
	- In C, working with dates and times is done via a specific header file, imported from the <time.h> header library.
		- Syntax:
			```
			#include <time.h>
			```
	- After importing the required header files, it is now possible to get the current time, format it, etc.
- Getting the current time
	- Definition:
		- The _time()_ function returns the current time, as a data type _time_t_.
	- Syntax:
		```
		time(&<variable>);
		```
	- Example:
		```
		time_t my_time;
		
		time(&my_time);
		```
- Breaking down the time
	- Definition:
		- It is possible to acess the individual parts of a date or time, like the year, month or day, or hour, minute or second.
		- Done using the _localtime()_ function, taking the current time from the _time()_ function into a _struct tm_ structure.
			- A special structure that holds the date and time into separate fields.
	- Syntax:
		```
		struct tm *<pointer_name> = localtime(<variable>);
		```
	- Example:
		```
		time_t my_time = time(NULL);
		struct tm *yes = localtime(&my_time); // localtime() returns a pointer to a struct t,
		
		printf("Year: %d\n", yes->tm_year + 1900); // since localdate returns the year since 1900
		printf("Month: %d\n", yes->tm_mon + 1); // months are ordered from 0 to 11
		printf("Day: %d\n", yes->tm_mday); // month day
		printf("Hour: %d\n", yes->tm_hour); // current hour
		printf("Minute: %d\n", yes->tm_min); // current minute
		printf("Second: %d\n", yes->tm_sec); // current second
		```
- Formatting date and time
	- Definition:
		- It is done through the _strftime()_ function, as ot formats the date and time into a string.
	- Syntax:
		```
		strftime(<buffer_variable>, <buffer_size>, <format>, <time_struct>);
		```
	- Example:
		```
		time_t my_time;
		time(&my_time);
		
		struct tm *yes = localtime(&my_time);
		char my_buffer[100];

		strftime(my_buffer, 100, "%d-%m-%Y %H:%M:%S", yes);
		```