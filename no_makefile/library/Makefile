CC:=gcc
CFLAGS:=-Wall -I`pwd` -L`pwd`
OBJS:=main.o file_reader.o
BIN:=main
LIB:=libfile_reader.so

all: $(BIN)

$(BIN): main.o $(LIB)
	$(CC) $(CFLAGS) -o $(BIN) main.o -lfile_reader

$(LIB): file_reader.o
	$(CC) $(CFLAGS) -o $(LIB) -shared -fpic $^

%.c: %.o
	$(CC) $(CFLAGS) -o $@ $^

compilelib: $(LIB)

$(LIB): file_reader.o
	$(CC) $(CFLAGS) -o $(LIB) -shared -fpic $^

clean:
	rm -f $(BIN) $(OBJS) $(LIB)

# LD_LIBRARY_PATH=`pwd` ./main
