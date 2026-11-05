# Libft

## Description

Libft is the first project of the 42 Common Core. The goal is to build, in C, a personal static library (`libft.a`) that reimplements a set of standard C library functions, adds a few extra utility functions, and provides basic linked-list management. The library is meant to be reused in all later 42 projects.

The project helps to understand how these functions work internally, how memory is handled (allocation, overlap, bounds), and how a static library is built and linked.

### Library description

The library is written in C, follows the 42 Norm, and compiles with `-Wall -Wextra -Werror`. It is split into four groups of functions.

**Part 1 – libc reimplementations** (same behavior as the originals, prefixed with `ft_`)

| Category | Functions |
|---|---|
| Character tests / conversion | `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower` |
| Strings | `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strdup`, `ft_atoi` |
| Memory | `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc` |

**Part 2 – Additional functions**

| Function | Description |
|---|---|
| `ft_substr` | Returns a substring of a string (allocated). |
| `ft_strjoin` | Concatenates two strings into a new one. |
| `ft_strtrim` | Removes a set of characters from the start and end of a string. |
| `ft_split` | Splits a string into an array of strings using a delimiter character. |
| `ft_itoa` | Converts an integer to an allocated string. |
| `ft_strmapi` | Applies a function to each character and returns the new string. |
| `ft_striteri` | Applies a function to each character (with its index) in place. |
| `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd` | Write a character, string, string + newline or number to a file descriptor. |

**Part 3 – Linked lists** (using `t_list`, with `content` and `next`)

`ft_lstnew`, `ft_lstadd_front`, `ft_lstadd_back`, `ft_lstsize`, `ft_lstlast`, `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`, `ft_lstmap`

All prototypes and the `t_list` type are declared in [libft.h](libft.h).

## Instructions

### Compilation

```sh
make          # builds libft.a
make clean    # removes object files
make fclean   # removes object files and libft.a
make re       # fclean + all
```

### Usage in a project

Include the header in your source files:

```c
#include "libft.h"
```

Then compile and link against the library (`-lft` must come after your source/object files):

```sh
cc -Wall -Wextra -Werror main.c -L. -lft -o program
```

If the library is in a `libft/` subfolder:

```sh
cc main.c -Ilibft -Llibft -lft -o program
```