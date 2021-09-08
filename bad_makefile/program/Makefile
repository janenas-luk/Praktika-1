CC:=gcc
CFLAGS:=-Wall -I`pwd` -L`pwd`
OBJS:=
BIN:=calculator
LIB:=libmath_functions.so

all: $(BIN)

$(BIN): main.c $(LIB)
	$(CC) $(CFLAGS) -o $(BIN) main.c -lmath_functions

$(LIB): math_functions.c
	$(CC) $(CFLAGS) -shared -fPIC -o $(LIB) $^

clean:
	rm -f $(BIN) $(OBJS) $(LIB)
