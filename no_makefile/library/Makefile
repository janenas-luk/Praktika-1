CC:=gcc
CFLAGS:=-Wall -I`pwd` -L`pwd`
OBJS:=main.o file_reader.o
BIN:=main
LIB:=libfile_reader.so

.PHONY: all clean install uninstall
	
all: $(BIN)

compilelib: $(LIB)

$(BIN): main.o $(LIB)
	$(CC) $(CFLAGS) -o $(BIN) main.o -lfile_reader

$(LIB): file_reader.o
	$(CC) $(CFLAGS) -o $(LIB) -shared -fpic $^

%.o: %.c
	$(CC) $(CFLAGS) -c -o $@ $^

install:

uninstall:

clean:
	rm -f $(BIN) $(OBJS) $(LIB)

# LD_LIBRARY_PATH=`pwd` ./main
