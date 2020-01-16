# A Makefile to generate executive file                                                                                                                                                   
# Copyright (C) 2014 shallnew \at 163 \dot com

CFLAGS += -g -Wall -Werror -O2
CPPFLAGS += -I. -I./inc -I../../include
LDFLAGS += -lpthread -L../../libs  


# SRC_OBJ = $(patsubst %.c, %.o, $(wildcard *.c))
SRC_FILES = $(wildcard *.c)
SRC_OBJ = $(SRC_FILES:.c=.o)  
SRC_BIN = app          

all : $(SRC_BIN)

$(SRC_BIN) : $(SRC_OBJ)       
	$(CC) -o $@ $^ $(LDFLAGS) 
	@echo -------- now is in main --------
	# mv $@ ../../.

obj : $(SRC_OBJ)

# clean target
clean:
	$(RM) $(SRC_OBJ) $(SRC_BIN) 

distclean:
	$(RM) $(SRC_OBJ) $(SRC_BIN)   tags*

.PHONY : all obj clean disclean 



gcc -o app app.c -L../../libs -lmath