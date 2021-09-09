CC:=gcc
CFLAGS:=-Wall -I`pwd` -L`pwd`
OBJS:=main.o maths.o usage.o
BIN:=calculator

.PHONY: all clean install uninstall

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) -o $(BIN) $^

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $^

install:

uninstall:

clean:
	rm -f $(BIN) $(OBJS)