# Libft (42)

A custom C utility library reimplementing common libc routines, created for the 42 curriculum.

## 📦 What’s inside

Core functions (selected):
- Memory: `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memccpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`
- Strings: `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`
- Char checks: `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`
- Case: `ft_toupper`, `ft_tolower`
- Conversion & alloc: `ft_atoi`, `ft_calloc`, `ft_strdup`
- Extra string utils: `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`, `ft_itoa`, `ft_strmapi`, `ft_striteri`
- File-descriptor helpers: `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`

Bonus (linked list):
- `ft_lstnew`, `ft_lstadd_front`, `ft_lstadd_back`, `ft_lstlast`, `ft_lstsize`


## 🛠 Tech

- **Language:** C
- **Build:** Makefile → static library 


## 🔧 Build

```bash
make        # builds libft.a
make clean  # remove object files
make fclean # remove objects + libft.a
make re     # rebuild
````


## ✅ Using Libft 

1. Copy `libft.a` and `libft.h` (or add this repository as a submodule).
2. Compile and link:

```bash
gcc -Wall -Wextra -Werror -I. main.c -L. -lft -o app
# if libft sources live in ./Libft, adapt include/lib paths accordingly
```

Example:

```c
#include "libft.h"
#include <stdio.h>

int main(void) {
    char *s = ft_strdup("hello");
    printf("%zu\n", ft_strlen(s));
    ft_putendl_fd(s, 1);
    return 0;
}
```

## 📂 Structure

- `libft.h` — public header
- `*.c` — implementation files
- `Makefile` — build rules
