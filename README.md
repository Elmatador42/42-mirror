# Libft

Bibliothèque C personnelle (projet 42) : réimplémentation de fonctions de la libc, fonctions utilitaires supplémentaires et gestion de listes chaînées. Le résultat est une bibliothèque statique `libft.a`.

## Contenu

- **Caractères** : `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint`, `ft_toupper`, `ft_tolower`
- **Chaînes** : `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strdup`, `ft_atoi`
- **Mémoire** : `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc`
- **Utilitaires** : `ft_substr`, `ft_strjoin`, `ft_strtrim`, `ft_split`, `ft_itoa`, `ft_strmapi`, `ft_striteri`
- **Sortie fichier** : `ft_putchar_fd`, `ft_putstr_fd`, `ft_putendl_fd`, `ft_putnbr_fd`
- **Listes chaînées** : `ft_lstnew`, `ft_lstadd_front`, `ft_lstadd_back`, `ft_lstsize`, `ft_lstlast`, `ft_lstdelone`, `ft_lstclear`, `ft_lstiter`, `ft_lstmap`

## Compilation

```sh
make        # génère libft.a
make clean  # supprime les fichiers objets
make fclean # supprime les objets et libft.a
make re     # recompile tout
```

Flags : `-Wall -Wextra -Werror`.

## Utilisation

```c
#include "libft.h"
```

```sh
cc main.c -L. -lft -o programme
```
