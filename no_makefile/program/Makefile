CC:=gcc
CFLAGS:=-Wall -I`pwd` -L`pwd`
OBJS:=main.o maths.o usage.o
BIN:=calculator

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) -o $(BIN) $^

%.c: %.o
	$(CC) $(CFLAGS) -o $@ $^

clean:
	rm -f $(BIN) $(OBJS)
