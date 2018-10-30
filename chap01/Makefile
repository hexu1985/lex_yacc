# Makefile

LEX = flex
RMR = rm -rf
RM = rm -f
CC = gcc

VPATH = 
CFLAGS = -Wall -g -DDEBUG 
INCLUDE = 
LDFLAGS = -lfl
LDPATH = 

PROGS = ch1-01.exe

.PHONY: all
all: $(PROGS)
	@echo "build OK!"

.PHONY: clean
clean:
	$(RM) $(PROGS) *.o *.obj *.exe *.l.c
	@echo "clean OK!"

%.l.c:%.l
	$(LEX) -o $@ $<

ch1-01.exe: ch1-01.l.c
	$(CC) -o $@ $^ $(LDFLAGS) $(LDPATH)

