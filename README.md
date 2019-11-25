# libft_abida
My implementation of some of the Standard C Library functions including some additional ones.

### Table of content
* [What is libft?](#what-is-libft)
* [What's in it?](#whats-in-it)
* [How does it work?](#how-does-it-work)
* [How do I use the library?](#how-do-i-use-the-library)


### What is libft?
Libft is an individual project at 1337 from 42 network that requires us to re-create some standard C library functions including some additional ones that can be used later to build a library of useful functions for the rest of the program.

### What's in it?

1.  **Libc Functions:** Some of the standard C functions
2.  **Additional functions:** Functions 42 deems will be useful for later projects
3.  **Bonus Functions:** Functions 42 deems will be useful for linked list manipulation

Libc functions | Additional functions | Bonus Functions
:----------- | :-----------: | :-----------:
memset		| ft_memalloc	| ft_lstnew		
bzero		| ft_memdel		| ft_lstdelone	
memcpy		| ft_strnew		| ft_lstdel		
memccpy		| ft_strdel		| ft_lstadd		
memmove		| ft_strclr		| ft_lstiter	
memchr		| ft_striter	| ft_lstmap		
memcmp		| ft_striteri	|				
strlen		| ft_strmap		|				
strdup		| ft_strmapi	|				
strcpy		| ft_strequ		|				
strncpy		| ft_strnequ	|			
strcat		| ft_strsub		| 
strlcat		| ft_strjoin	| 
strchr		| ft_strtrim	| 
strrchr		| ft_strsplit	| 
strstr		| ft_itoa		| 
strnstr		| ft_putchar	| 
strcmp		| ft_putstr		| 
strncmp		| ft_putendl	|
atoi		| ft_putnbr		| 
isalpha		| ft_putchar_fd	| 
isdigit		| ft_putstr_fd	| 
isalnum		| ft_putendl_fd	| 
isascii		| ft_putnbr_fd	| 
isprint		| 
toupper		| 
tolower		| 


Notes:

- Most of the the files and function names are namespaced with an **ft** in front. It stands for Fourty Two
- The project instructions require that we put all the source files in the root directory.

Bare in mind that my code is not the best ;).

### How does it work?

The goal is to create a library called libft.a from the source files so I can later use that library from other projects at 1337 cursus.

To create that library, after downloading/cloning this project, **cd** into the project and call make:

	git clone https://github.com/abdoabida/libft_abida.git
	cd libft_abida
	make

You should see a *libft.a* file and some object files (.o).

Now to clean up (removing the .o files), call `make clean`

### How do I use the library?

I added a test file called **test.c**, it's using functions from the library to print the length of a string given as a parameter 

If you try to compile it with gcc using `gcc test.c` you will get an *undefined symbol* error for the functions used. 

You have to give the file the path of the library and which library it is using:

`gcc test.c -L. -lft`

-L takes the path to your library. `.` in this case<br>
-l takes the name of your library. This is the set of characters that come after `lib` in your library name.

That's it. Now run it using `./a.out`

Enjoy.