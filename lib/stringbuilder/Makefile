NAME = lib_string_builder.a	
SRC = ./srcs/fragment.c  ./srcs/string_builder.c

LIBFT = ../libft/includes/
TRY_CATCH = ../try_catch/includes/
ARRAY_LIST = ../arraylist/includes/

# SRC += -L ../arraylist/arraylist.a 

CC = gcc	
FLAGS= -Wall -Werror -Wextra 	
PARA  = -c	
OBJ= $(SRC:.c=.o)
INC = ./includes/  \
			-I $(LIBFT) \
			-I $(ARRAY_LIST) \
			-I $(TRY_CATCH)

%.o: %.c
	$(CC) $(PARA) $(SRC) -I $(INC)  -I $(TRY_CATCH)  $<
	
array_list:
	$(MAKE) -C ../arraylist/ 

all: $(NAME)	

$(NAME): $(array_list) $(OBJ)
	ar rc $(NAME)   ./string_builder.o ./fragment.o

clean:	
	rm -f  $(OBJ)

fclean: clean	
	rm -f $(NAME)	
	rm -f includes/*.*.gch	

re: fclean all

