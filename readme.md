```

#Link from website: https://stackoverflow.com/questions/13664693/makefile-compiling-and-linking
#Q1: How to write the Makefile

#I have the following Makefile:

CC = gcc
CFLAGS = -Wall -Werror -Wmissing-prototypes
OBJS = server.o rio.o

all: $(OBJS)
    $(CC) $(CFLAGS) $(OBJS) -o sysstatd

server.o: server.c
    $(CC) $(CFLAGS) -c server.c

rio.o: rio.c rio.h
    $(CC) $(CFLAGS) -c rio.c

clean:
    rm -f *~ *.o sysstatd

```
