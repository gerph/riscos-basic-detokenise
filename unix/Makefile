CC = gcc
LIBS =
INCS =
CDEFINES =
CFLAGS = -g $(INCS)

FILES = \
	basic.c basic.h main.c memory.c \
	memory.h VersionLog VersionNum

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
	ln -sf ../c/basic basic.c
basic.h: ../h/basic
	ln -sf ../h/basic basic.h
main.o: main.c basic.h memory.h VersionNum
main.c: ../c/main
	ln -sf ../c/main main.c
memory.c: ../c/memory
	ln -sf ../c/memory memory.c
memory.h: ../h/memory
	ln -sf ../h/memory memory.h
VersionLog: ../VersionLog
	ln -sf ../VersionLog VersionLog
VersionNum: ../VersionNum
	ln -sf ../VersionNum VersionNum
