
# List (ls)
- Definition:
	- Used to list the contents of a directory.
	- Can list files, folders, and even information about said contents.
- Syntax:
```
ls <folder>
#> or
ls <options> <folder>
```
- Example:
```
ls
#> or
ls my_folder/
```
- Options:
	- -l
		- Definition:
			- Enables the long listing format.
			- Displays these information:
				- File or folder name.
				- File permissions.
				- Number of links.
				- Owners name.
				- Owners group
				- File size.
				- Time of last modification.
		- Syntax:
			```
			ls -l
			```
	- -a
		- Definition:
			- Toggles hidden files, files that start with a dot _._.
			- Enables to listing of dotfiles since by default, _ls_ does not list them.
		- Syntax:
			```
			ls -a
			```
	- -h
		- Definition:
			- Enables human-readable sizes, converts byte counts into readable formats like Kilobytes (K), Megabytes (M), etc.
			- This option is commonly used with the -l option.
		- Syntax:
			```
			ls -lh
			```
	- -t
		- Definition:
			- Enables sorting by time, used to query the latest files.
			- Specifically, modification time.
		- Syntax:
			```
			ls -t
			```
	- -r
		- Definition:
			- Enables reverse sorting, i.e. flips the current sorting order.
		- Syntax:
			```
			ls -r
			```
	- -R
		- Definition:
			- Enables recursive listing, i.e. lists files and folders inside of folders.
		- Syntax:
			```
			ls -R
			```
	- -S
		- Definition:
			- Enables sorting by size, i.e. sorts the files by largest first.
		- Syntax:
			```
			ls -S
			```
	- -1
		- Definition:
			- Lists contents per line, i.e. one line per element.
		- Syntax:
			```
			ls -1
			```
	- -d
		- Definition:
			- Lists only directories, does not list any files.
		- Syntax:
			```
			ls -d
			```
	- -F
		- Definition:
			- Appends an indicator for certain files, e.g. * for executables (.sh).
		- Syntax:
			```
			ls -F
			```