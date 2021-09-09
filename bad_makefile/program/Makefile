CC:=gcc
CFLAGS:=-Wall -I`pwd` -L`pwd`
OBJS:=math_functions.o main.o
BIN:=calculator
LIB:=libmath_functions.so

.PHONY: all clean install uninstall
	
all: $(BIN)

$(BIN): main.o $(LIB)
	$(CC) $(CFLAGS) -o $(BIN) $< -lmath_functions

main.o: main.c
	$(CC) $(CFLAGS) -c -o $@ $^

$(LIB): math_functions.o
	$(CC) $(CFLAGS) -shared -fPIC -o $(LIB) $^

math_functions.o: math_functions.c
	$(CC) $(CFLAGS) -c -o $@ $^

install:

uninstall:

clean:
	rm -f $(BIN) $(OBJS) $(LIB)

# LD_LIBRARY_PATH=`pwd` ./calculator
