CC:=gcc
CFLAGS:=-Wall
LIB:=calculator.so

all: $(LIB)

$(LIB): math_functions.c
	$(CC) $(CFLAGS) -shared -fPIC -o $(LIB) $^

install: $(LIB)
	install -m 644 math_functions.h $(DESTDIR)/$(PREFIX)/include

uninstall:

clean:
	rm -f $(LIB)
