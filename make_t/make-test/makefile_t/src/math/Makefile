# A Makefile to generate archive file
# Copyright (C) 2014 shallnew \at 163 \dot com


CFLAGS += -g -Wall -Werror -O2 -shared -fPIC
CPPFLAGS += -I. -I./inc -I../../include

# SRC_OBJ = $(patsubst %.c, %.o, $(wildcard *.c))
SRC_FILES = $(wildcard *.c)
SRC_OBJ = $(SRC_FILES:.c=.so)


# SRC_LIB =  -lpthread

all:$(SRC_OBJ)

$(SRC_OBJ):$(SRC_FILES) 
	@echo ================================================================= 
	$(CC) $(CFLAGS)  -o $@ $^
	mv $@ ../../libs
	rm -rf *dSYM
	@echo ================================================================= 	
obj : $(SRC_OBJ)
 
clean:
	$(RM) $(SRC_OBJ) $(SRC_LIB)

distclean:
	$(RM) $(SRC_OBJ) $(SRC_LIB) tags  
.PHONY : all obj clean disclean 


 