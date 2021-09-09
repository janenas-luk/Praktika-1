CC:=gcc
CFLAGS:=-Wall
LIB:=calculator.so
OBJS:=math_functions.o

.PHONY: all install uninstall clean

all: $(LIB)

$(LIB): math_functions.o
	$(CC) $(CFLAGS) -shared -fPIC -o $(LIB) $^

math_functions.o: math_functions.c
	$(CC) $(CFLAGS) -c -o $@ $^

install: $(LIB)
	install -m 644 math_functions.h $(DESTDIR)/$(PREFIX)/include

uninstall:

clean:
	rm -f $(LIB) $(OBJS)
