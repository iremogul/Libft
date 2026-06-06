*This project has been created as part of the 42 curriculum.*

# Libft

## Description
Libft is the first project of the 42 curriculum where we recode many of the standard C library (libc) functions alongside various additional utility functions. The goal is to create our own reliable, optimized, and standard-compliant static library (`libft.a`) to serve as a foundational toolset for all future projects. 

Through this project, a deep understanding of memory allocation, string manipulation, and the inner workings of standard C functions is achieved.

---

## Contents and Functions
This library contains functions categorized into two main groups according to the mandatory part requirements:

### 1. Libc Functions
Recoded versions of the fundamental functions found in the standard C library:
* **Character Checks and Conversions:** `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower`
* **String Operations:** `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`
* **Memory Operations:** `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
* **Conversion and Dynamic Memory Allocation:** `ft_atoi`, `ft_calloc`, `ft_strdup`

### 2. Additional Functions
Utility functions that are not part of the standard library but are frequently needed in 42 projects:
* **String Manipulation:** `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`
* **Conversions and Iterations:** `ft_itoa`, `ft_strmapi`, `ft_striteri`
* **File Descriptor Outputs:** `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

---

## Instructions

### Compilation
To compile the library and create the `libft.a` static library file, simply navigate to the root directory of the project in your terminal and run the following command:
make

This process will compile all your `.c` source files with `-Wall -Wextra -Werror` flags, making the library ready to use. To clean up after compiling your project, you can use the following rules:
* `make clean`: Removes only the compiled object files (`.o`).
* `make fclean`: Removes the object files as well as the generated `libft.a` file.
* `make re`: Completely cleans everything and recompiles the library from scratch.

### Usage
To use the generated `libft.a` file in your own C projects:
1. Include the `libft.h` header file in your relevant code as `#include "libft.h"`.
2. Link the library to the compiler when compiling your code:
gcc main.c -L. -lft

---

## Resources & AI Usage
* **Core References:** Linux manual pages and C programming standards.
* **AI Usage:** During the development process, AI tools were used to brainstorm the setup of the Makefile, generate logical outlines for functions requiring complex memory management like `ft_split`, and obtain conceptual explanations regarding pointer arithmetic. No generated solutions were directly copy-pasted into the project; each function was subjected to manual testing and integrated into the codebase only after its underlying mechanism was fully understood.
