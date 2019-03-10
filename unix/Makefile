CDEFINES =
CFLAGS = -g

LIBS =
OBJS = \
  basic.o \
  main.o \
  memory.o

all: bastotxt

clean:
	-rm -f *.o *.c *.cpp *.h Version*

.c.o:
	cc $(CFLAGS) $(CDEFINES) -c -o $@ $?

bastotxt: $(OBJS) $(LIBS)
	cc -g -o bastotxt $(OBJS) $(LIBS)
