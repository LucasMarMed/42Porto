# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lumarque <lumarque@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/04/16 14:47:25 by lumarque          #+#    #+#              #
#    Updated: 2023/05/06 15:32:25 by lumarque         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a
SRC = ft_atoi.c ft_strlen.c ft_bzero.c ft_memset.c ft_calloc.c ft_isalnum.c \
		ft_isalpha.c ft_isascii.c ft_isdigit.c ft_isprint.c ft_memchr.c \
		ft_memcmp.c ft_split.c ft_putchar_fd.c ft_putstr_fd.c ft_memcpy.c \
		ft_memmove.c ft_putendl_fd.c ft_strchr.c ft_putnbr_fd.c \
		ft_strdup.c ft_strjoin.c ft_strlcat.c ft_strlcpy.c ft_strncmp.c \
		ft_strnstr.c ft_strrchr.c ft_substr.c ft_tolower.c ft_toupper.c \
		ft_strmapi.c ft_striteri.c ft_itoa.c ft_strtrim.c
OBJS = ${SRC:.c=.o}

BONUS_S	= ft_lstsize.c ft_lstlast.c ft_lstadd_front.c ft_lstadd_back.c \
			ft_lstnew.c ft_lstdelone.c ft_lstclear.c ft_lstiter.c ft_lstmap.c
BONUS_O	= $(BONUS_S:.c=.o)

INCLUDE = libft.h
CC = gcc
RM = rm -f
CFLAGS = -Wall -Wextra -Werror

${NAME}: ${OBJS}
	ar -rcs ${NAME} ${OBJS} ${INCLUDE}

all: ${NAME}

bonus:	$(NAME) $(BONUS_O)
		ar -rcs $(NAME) $(BONUS_O) ${INCLUDE}

clean: 
	${RM} ${OBJS}

fclean: clean
	${RM} ${NAME} $(BONUS_O) teste

re: fclean all

rebonus:	fclean bonus

teste: fclean
	${CC} ${CFLAGS} ${INCLUDE} main.c ${NAME} -o teste

.PHONY: all clean fclean re
