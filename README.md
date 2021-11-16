# Asemmbler simulation project
This project is an assignment in a C programming course at the open unvieristy.
The porpuse of the project is to demonstrate how assembler works:
- gets assembly code files
- detects any illeagal coding 
- prints error massages if needed
- prints a machine code file 
- prints an entry labels table file
- prints an external labels table file

## Installation

The project runs on linux operating system .
The project was created on a 32 bit opeating system but works also on a 64 bit operating systems.

## Source structure (Modules)
1. `assembler.c` - main function definition, argv & argc processing.
2. `first_reading.c` - contains functions for processing the first reading of the assembly file.
3. `second_reading.c` - contains functions for processing the second reading of the assemblt file.
4. `command_help.c` - contains useful functions for detecting and handling commands in the assembly code.
5. `directive_help.c` - contains useful functions for detecting and handling directives in the assembly code .
6. `label_help.c` - contains functions helping detect labels and labels errors.
7. `functions_for_commands_and_directives_reading.c` - contains general functions helping proccess the assembly code.
8. `command_table.c`- contains the commands codes - all the other files use the information that in this table to translte the assembly code to a machine code 
9. `create_files.c` - contains the functions that printing the output files.
10. `free_memory.c` - contains the functions helping free all the allocated memory in the project.


## Usage
`./assembler file1.as file2.as file3.as ...`
Will start the processing of each file (specify WITHOUT extension!).

## Build
You may build with several tools:
1. Using CMake: run `cmake --build .` (you might have to run `cmake --cofngiure .` first) - Provides support for CLion IDE
2. Using `make` command (Makefile)
3. Manually (Not recommended): compile each `*.c` file to `*.o` and then compile all to a single executable using `CC`/`GCC`/`CLang` with `-g a.o b.o .... -o exe
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
