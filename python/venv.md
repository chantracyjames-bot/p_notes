
# Virtual Environments
- Definition
	- It is an isolated environment in Python, used to run and test Python projects.
	- It enables management of project-specific dependencies (projects), all while not interfering with other projects' dependencies or the original Python installation.
	- Analogy:
		- A virtual environment is a separate container for each Python project, where each container has its own Python interpreter (similar to compilers).
		- It has it's own set of installed packages and can have different versions of the same package, all while being isolated from other containers.
	- Importance:
		- It prevents package conflicts between projects.
		- Allows projects to be more portable and reproducible.
		- Keeps the original Python installation to be clean.
		- Allows testing with different Python versions.
- Creating a virtual environment:
	- Definitin:
		- It is typically done through the terminal, or the command line.
	- Syntax:
		```
		python -m venv <venv_name>
		```
	- Example:
		```
		pythom -m venv my_project
		```
	- Initial file structure:
		```
		<venv_name>
			|--> bin
			|--> include
			|--> lib
			|--> lib64
			|--> .gitignore
			\--> pyvenv.cfg
		```
- Activating a virtual environment:
	- Definition:
		- Acticating the virtual environment is done with a command.
	- Note
		- After activation, it is not possible to install packages independent of the original Python.
	- Syntax:
		```
		#> on Linux/macOS
		<venv_path>/bin/activate
		#> on Windows
		<venv_path>\Scripts\activate
		```
- Deactivating a virtual environment
	- Definition:
		- Deactivating the virtual environment is done with a command.
	- Note:
		- All modules that were installed in the virtual environment won't exist outside it.
	- Syntax:
		```
		deactivate
		```