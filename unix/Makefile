CC = gcc
CDEFINES =
CFLAGS = -g

FILES = \
	basic.c basic.h main.c memory.c \
	memory.h VersionLog VersionNum

LIBS =
OBJS = \
  basic.o \
  main.o \
  memory.o

.PHONY: all links

all: bastotxt
links: $(FILES)

clean:
	-rm -f *.c *.h VersionLog VersionNum *.o bastotxt

%.o: %.c
	$(CC) $(CFLAGS) $(CDEFINES) -c -o $@ $<

bastotxt: $(OBJS) $(LIBS)
	$(CC) -g -o bastotxt $(OBJS) $(LIBS)

# Links
basic.o: basic.c basic.h
basic.c: ../c/basic
	ln -s ../c/basic basic.c
basic.h: ../h/basic
	ln -s ../h/basic basic.h
main.o: main.c basic.h memory.h VersionNum
main.c: ../c/main
	ln -s ../c/main main.c
memory.c: ../c/memory
	ln -s ../c/memory memory.c
memory.h: ../h/memory
	ln -s ../h/memory memory.h
VersionLog: ../VersionLog
	ln -s ../VersionLog VersionLog
VersionNum: ../VersionNum
	ln -s ../VersionNum VersionNum
